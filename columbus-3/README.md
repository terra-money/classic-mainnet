## Genesis
Downlaod the columbus-3 genesis [Here](https://columbus-genesis.s3-ap-northeast-1.amazonaws.com/genesis.json)

## Genesis Parameters

Parameters that have been updated from `Columbus-2` have been highlighted.

### Slashing Module

- `"slash_fraction_double_sign": "0.05"`. Increase slashing fraction for the Validators who equivocate (double-sign a block, and thereby compromise safety) and are caught to 5%.

### Goverance Module

- `"min_deposit": "512luna"`. The minimum deposit to bring a proposal up for a vote is 512 LUNAs. Because the price of LUNAs is uncertain at launch, this value should be high enough to prevent spam proposals, while not being too expensive. As a note, the deposit can be crowd-funded, so the proposer doesn't have to provide the whole thing. Proposals which pass refund all deposits.
- `"max_deposit_period": "1209600000000000"`. The duration in which a proposal can collect deposits is 2 weeks. This value should be long enough for a proposal to have time to gain support from the community.
- `"voting_period": "1209600000000000"`. The duration in which a proposal can be voted upon is 2 weeks. The voting period should be long enough that all staked LUNA holders had time to participate.
- `"quorum": "0.4"`. A minimum quorum of 40% of bonded stake must vote on a proposal in order for it to be considered for passage. This is to ensure that proposals don't pass that have support from only a small segment of the community.
- `"threshold": "0.5"`. Over half the voting stake must vote in favor of a proposal in order for it to pass.
- `"veto": "0.334"`. 1/3 of voting stake vetoing a proposal prevents it from passing. This is necessitated by the 1/3 BFT safety bound, since 1/3 of stake could also elect to halt the chain or compromise safety.

### Market Module

- `"base_pool": "250000000000"`. Initial starting size of both Terra and Luna liquidity pools is 250,000 SDT.
- `"pool_recovery_period": 14400"`. The duration in which the Terra & Luna pools to naturally "reset" toward equilibrium (delta \~= 0) through automated pool replenishing is 14400 blocks (\~= a day).
- `"min_spread": "0.02"`. Minimum spread charged on Terra<>Luna swaps is 2%. This is to prevent leaking value from front-running attacks.
- `"tobin_tax": 0.0025`. A fee of 0.25% of swap amount is charged on swap between Terra currencies (spot-trading).
- `"illiquid_tobin_tax_list": [{'denom':'umnt','tax_rate':'0.02'}]`. Charge high tobin tax (2%) to the illquid denom (`umnt`).

### Oracle Module

- `"vote_period": "5"`. Shorten the oracle tally period to 5 blocks.
- `"reward_band": "0.07"`. Increase the criteria for receiving rewards and avoiding penalties to 7%, allowing validators to adapt to the initial improved penalty system.
- `"whitelist": ["ukrw", "usdr", "uusd", "umnt"]`. The list of currencies that can be voted on. This is set to (KRT, SDT, UST, MNT).
- `"reward_distribution_window": "5256000"`. The number of blocks during which oracle reward comes in and then is distributed is 5,256,000 blocks (\~= a year).
- `"slash_window": "432000"`. The number of blocks for slashing tallying is 432,000 blocks (\~= a month). 
- `"slash_fraction": "0.0001"`. The validators will get 0.01% penalty on bonded tokens for oracle voting violation.
- `"min_valid_per_window": "0.05"`. The validators should submit 5% valid votes per slash window to avoid slashing.


### Treasury Module

- `"tax_policy.rate_min": 0.001`. Minimum tax rate is increased to 0.1%.
- `"reward_policy.rate_max": 0.5`. Maximum reward weight is decreased to 50%.
- `"window_probation": "0"`. No mature period will be required for columbus-3.
