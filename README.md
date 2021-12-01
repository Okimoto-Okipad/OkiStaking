# OkipadStakingScilla
Scilla codes for Okipad Token Staking Contract


okipad testnet: 0x43cb4182401336fab00bdcda1fc150851d9c3cbd
<br>
https://viewblock.io/zilliqa/address/zil1g095rqjqzvm04vqtmndpls2ss5wec09ae950h5?network=testnet
<br>
staking: https://viewblock.io/zilliqa/address/zil1k85j7m7q9khjzp7j8gjnqpayvfw6rkssnxwag7?network=testnet
<br>
future: https://devex.zilliqa.com/address/0x4ce0291f3d6f98dec8c6158820bdf425b41ebea0?network=https://dev-api.zilliqa.com

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

