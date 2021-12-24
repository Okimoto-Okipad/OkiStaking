# OkipadStakingScilla
Scilla codes for Okipad Token Staking Contract


okipad testnet: 0x43cb4182401336fab00bdcda1fc150851d9c3cbd
<br>
https://viewblock.io/zilliqa/address/zil1g095rqjqzvm04vqtmndpls2ss5wec09ae950h5?network=testnet
<br>
staking: 0xb1C830b04eAf7De93a425F162C1B934943F02ec6
https://viewblock.io/zilliqa/address/zil1k8yrpvzw4a77jwjztutzcxunf9plqtkxzqzm40?network=testnet

testnet launchpad: 0xf1fcb773188cdbbb6fb74b17cb4c3d7d17e212bc
https://viewblock.io/zilliqa/address/zil1787twucc3ndmkmahfvtuknpa05t7yy4up57e97?network=testnet

<br>
future: https://devex.zilliqa.com/address/0x4ce0291f3d6f98dec8c6158820bdf425b41ebea0?network=https://dev-api.zilliqa.com

okipad mainnet: 0x54aE64e2092749fb8d25470ffc1d4D6A19c6f2Ab
https://viewblock.io/zilliqa/address/zil12jhxfcsfyaylhrf9gu8lc82ddgvudu4tzvduum

staking mainnet: 0xce7b758d08b477ef4f957fd7be81bb5e0976dcbc
https://viewblock.io/zilliqa/address/zil1eeahtrggk3m77nu40ltmaqdmtcyhdh9ujahgf6
## Examples

The mainnet carbon contract might be useful:
https://viewblock.io/zilliqa/address/zil18r37xks4r3rj7rzydujcckzlylftdy2qerszne?tab=tokens

Do Raise any issues found via the issues section

TestCases done on new contract:

TransferStakeToNewContract
- Only owner is able to call
- Data cycleCount, cycleAmount, Stakers balance passed over

TransferUnstakeToNewContract
- Only Owner is able to call
- Data removeStaker, removeBlock
RewardAll
- Correct Amount given to all, in totalStaked increased and ownerAvailable decreased correctly

addStakeForOther
- Overwrite if transition is called by same sender 2 times latest address is capture with amount
- Transferred to contract wrong amount will reject the transaction
- Transferred to contract the right amount pending is gone, correct amount is given to the address pending.
- If whitelisting is in effect, the pending address also has to be whitelisted
- if address already has staked, it will add on to their stake

withdrawal functions
- withdrawStake working
- RemoveStake working
- instantWithdrawal

When removed totalStaked and totalUnstaked is adjusted accordingly
totalStakers number is also accurate

Added pending to other addresses
tried to send wrong amount (Failed)
If correct amount sent, the stake is added in for the pending address



Remove pending if change of mind

rewardCycle seperated into new transition
If rewardCycle count not met no rewards is given


Calculated rewardsAll given and deducted from owner correctly
Calculated rewardCycle given and deducted from owner correctly



Tested whitelisting

