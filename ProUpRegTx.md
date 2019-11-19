```
A Provider Update Registrar Transaction (ProUpRegTx) is used to update information relating to the owner. An owner can update the operator's BLS public key (e.g. to nominate a new operator), the voting address and their own payout address.  Dash Core allows us to run the following command if we ant to update this information:

protx update_registrar proTxHash operatorKeyAddr votingKeyAddr payoutAddress (feeSourceAddress)

Where:
* proTxHash: The transaction id of the initial ProRegTx
* operatorKeyAddr: An updated BLS public key, or "" to use the last on-chain operator key
* votingKeyAddr: An updated voting key address, or "" to use the last on-chain voting key
* payoutAddress: An updated Dash address for owner payments, or "" to use the last on-chain operator key
* feeSourceAddress (optional): An address used to fund ProTx fee. PayoutAddress will be used if not specified.

In order to accomplish your goal and update the payout address for these 3 nodes, you have to use the dash core wallet you used to generate your ownerKeyAddr, and it has to be unlocked and then run the following commands from the Dash Core:

protx update_registrar 2ca020f7b546184b14d752a7b119369a39cb783fd6a64663e03a309d0138a0eb "" "" Xy8J3NTQFn7e8t22punvF89mYfX1MFzYYa

protx update_registrar b1947a03974d316e098387f26a468b37da091cc0e9b4c46fd3bc4be911264a85 "" "" Xy8J3NTQFn7e8t22punvF89mYfX1MFzYYa

protx update_registrar 44392dd46a9817988e4be01fb47855b4a2c924ff65c9217cbd896380ab0512d2 "" "" Xy8J3NTQFn7e8t22punvF89mYfX1MFzYYa

```
