# OkipadStakingScilla
Scilla codes for Okipad Token Staking Contract


okipad testnet: 0x43cb4182401336fab00bdcda1fc150851d9c3cbd
<br>
https://viewblock.io/zilliqa/address/zil1g095rqjqzvm04vqtmndpls2ss5wec09ae950h5?network=testnet
<br>
staking: 0xb1C830b04eAf7De93a425F162C1B934943F02ec6
https://viewblock.io/zilliqa/address/zil1k8yrpvzw4a77jwjztutzcxunf9plqtkxzqzm40?network=testnet

testnet launchpad: 0x565f79c6a0f884090c05ece49678383d7fc31ad4 
https://viewblock.io/zilliqa/address/zil12e0hn34qlzzqjrq9anjfv7pc84luxxk5933hjj?network=testnet&tab=state

<br>
future: https://devex.zilliqa.com/address/0x4ce0291f3d6f98dec8c6158820bdf425b41ebea0?network=https://dev-api.zilliqa.com

okipad mainnet: 0x54aE64e2092749fb8d25470ffc1d4D6A19c6f2Ab
https://viewblock.io/zilliqa/address/zil12jhxfcsfyaylhrf9gu8lc82ddgvudu4tzvduum

staking mainnet: 0xce7b758d08b477ef4f957fd7be81bb5e0976dcbc
https://viewblock.io/zilliqa/address/zil1eeahtrggk3m77nu40ltmaqdmtcyhdh9ujahgf6

Test Launchpad (Mainnet):
0xed56582a655762c4281096bd028a364ad947e30b
https://viewblock.io/zilliqa/address/zil1a4t9s2n92a3vg2qsj67s9z3kftv50cct2kq7xq

Test Coin (Mainnet): 0xc9cc9c8196901cfa09ee4f5aad19d5b1e05fc884
https://viewblock.io/zilliqa/address/zil1e8xfeqvkjqw05z0wfad26xw4k8s9ljyy3kj4xu

Final Launchpad (Mainnet HOL):
0x79d4f98f6062f342993cbbef61b6aa9097b9738f
https://viewblock.io/zilliqa/address/zil10820nrmqvte59xfuh0hkrd42jztmjuu0u39kn3?tab=state

HoL Coin (Mainnet):
0x9945a0da3dc74e364da4ea96946c99336013eeb5
https://viewblock.io/zilliqa/address/zil1n9z6pk3aca8rvndya2tfgmyexdsp8m44gpyrs3?tab=state
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

