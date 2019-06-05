## Upgrade Instructions

The following document describes the necessary steps involved that a full node must take in order to upgrade from `columbus-1` to `columbus-2`. The Terra team will post an official updated genesis file, but it is recommended that validators execute the following instructions in order to verify the resulting genesis file.

## Risks

As a validator performing the upgrade procedure on your consensus nodes carries a heightened risk of double-signing and being slashed. The most important piece of this procedure is verifying your software version and genesis file hash before starting your validator and signing.

The riskiest thing a validator can do is discover that they made a mistake and repeat the upgrade procedure again during the network startup. If you discover a mistake in the process, the best thing to do wait for the network to start before correcting it. If they network is halted and you have started with a different genesis file than the expected one, seek advice from a Terra Core developer on discord before resetting your validator.

## Changes

Release v0.2.0 will contain the correct version for `columbus-2`. 
The [Changelog](https://github.com/terra-project/core/tree/master/CHANGELOG.md) will be updated to reflect the changes.  

## Upgrade Steps

1. The version of the core, v0.2.0, which currently all full nodes in the network run, contains a zero height export bug related to distribution and vesting account. This bug has been fixed in a hotfix release v0.2.0 (TODO). (skip this step if you already have v0.2.0+)
    1. Checkout and install the v0.2.0 release
        ```
        $ git checkout master; git pull; make
        ```
    2. Verify the binary versions
        ```
        $ terracli version --long
        core: 0.2.0
        git commit: 27cabafca9309cb0d176dc60f367adbdf5911e9a
        go.sum hash: 66dc7d804e4b546420aa507f5e7f861f0e6ed5de1ee3428276f3e5e0858f37f7
        build tags: netgo ledger
        go version go1.12.5 darwin/amd64
        ```

        ```
        $ terrad version --long
        core: 0.2.0
        git commit: 27cabafca9309cb0d176dc60f367adbdf5911e9a
        go.sum hash: 66dc7d804e4b546420aa507f5e7f861f0e6ed5de1ee3428276f3e5e0858f37f7
        build tags: netgo ledger
        go version go1.12.5 darwin/amd64
        ```

2. Export existing state from `columbus-1`.
    1. Export genesis state to file
        ```
        terrad export --for-zero-height --height=580000 > columbus-1-genesis-export.json
        ```
    2. Verify the SHA256 of the (sorted) generated export file
        ```
        jq -S -c -M '' columbus-1-genesis-export.json | shasum -a 256
        a538974a229fa1118e0511bb1441f02afcb9c99e0c274ba8a0921ac4fa1a0b0e
        ```
3. The exported genesis state generated in step (2) must now be modified to include the modified vesting schedules for the several accounts.
    ``` 
    python3 contrib/export/columbus1-to-columbus2.py columbus-1-genesis-export.json contrib/export/i-4-vesting-type-accounts.csv --chain-id=columbus-2 --start-time=2019-06-06T06:00:00Z | jq -S -c -M '' > genesis.json
    ```
4. Verify the SHA256 of the final genesis JSON
   ```
   sha256sum genesis.json
   8166ebb40a9f6cab96994d56aa8183e0686f9863d6dd58d00053073cf4a6bb88  genesis.json
   ```
5. Reset state
   ```
   terrad unsafe-reset-all
   ```
6. Restart the node!
