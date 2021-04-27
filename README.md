# CarbonStakingScilla
Scilla codes for Carbon Token Staking Contract


carbon testnet: 0x3e1b442f12c57449464c7daa162803765606b81f
<br>
https://viewblock.io/zilliqa/address/0x3e1b442f12c57449464c7daa162803765606b81f?network=testnet 
<br>
testnet : 0xa26cb7d77bc6c4b47ed0e6c4209e61be33ef822f <br>
https://viewblock.io/zilliqa/address/zil15fkt04mmcmztglksumzzp8nphce7lq3096048g?network=testnet

Do Raise any issues found via the issues section

TestCases done on new contract:
Added pending to other addresses
tried to send wrong amount (Failed)
If correct amount sent, the stake is added in for the pending address
if address already has staked, it will add on to their stake
If whitelisting is in effect, the pending address also has to be whitelisted

Remove pending if change of mind

rewardCycle seperated into new transition
If rewardCycle count not met no rewards is given


Calculated rewardsAll given and deducted from owner correctly
Calculated rewardCycle given and deducted from owner correctly

Tested instantWithdrawal
Tested withdrawStake when blocks are reduced to 1

Tested whitelisting

