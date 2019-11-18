## Genesis Parameters

Parameters that have been updated from `Columbus-2` have been highlighted.


### Goverance Module

- `"min_deposit": "512luna"`. The minimum deposit to bring a proposal up for a vote is 512 LUNAs. Because the price of LUNAs is uncertain at launch, this value should be high enough to prevent spam proposals, while not being too expensive. As a note, the deposit can be crowd-funded, so the proposer doesn't have to provide the whole thing. Proposals which pass refund all deposits.
- `"max_deposit_period": "172800000000000"`. The duration in which a proposal can collect deposits is 2 days. This value should be long enough for a proposal to have time to gain support from the community.
- `"voting_period": "172800000000000"`. The duration in which a proposal can be voted upon is 2 days. The voting period should be long enough that all staked LUNA holders had time to participate.
- `"quorum": "0.4"`. A minimum quorum of 40% of bonded stake must vote on a proposal in order for it to be considered for passage. This is to ensure that proposals don't pass that have support from only a small segment of the community.
- `"threshold": "0.5"`. Over half the voting stake must vote in favor of a proposal in order for it to pass.
- `"veto": "0.334"`. 1/3 of voting stake vetoing a proposal prevents it from passing. This is necessitated by the 1/3 BFT safety bound, since 1/3 of stake could also elect to halt the chain or compromise safety.

### Market Module

- `base_pool: "250000000000"`. Initial starting size of both Terra and Luna liquidity pools is 250,000 SDT.
- `pool_recovery_period: 14400"`. The duration in which the Terra & Luna pools to naturally "reset" toward equilibrium (delta \~= 0) through automated pool replenishing is 14400 blocks (\~= a day).
- `min_spread": "0.02"`. Minimum spread charged on Terra<>Luna swaps is 2%. This is to prevent leaking value from front-running attacks.
- `"tobin_tax": 0.0025`. A fee of 0.25% of swap amount is charged on swap between Terra currencies (spot-trading).

### Oracle Module

- `whitelist: ["ukrw", "usdr", "uusd", "umnt"]`. The list of currencies that can be voted on. This is set to (KRT, SDT, UST, MNT).
- `reward_distribution_window: "86400"`. The number of vote periods during which oracle reward comes in and then is distributed is 86,400 vote periods (\~= a month).
- `slash_window: "2880"`. The number of vote periods for slashing tallying is 2,880 vote periods (\~= a day). 
- `slash_fraction: "0.0001"`. The validators will get 0.01% panelty on bonded tokens for oracle voting violation.
- `min_valid_per_window: "0.05"`. The validators should submit 5% valid votes per slash window to avoid slashing.


### Treasury Module

- `"tax_policy.rate_mint": 0.005`. Minimum tax rate is increased to 0.5%.
