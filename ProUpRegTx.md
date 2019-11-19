# Provider Update Registrar Transaction

A Provider Update Registrar Transaction (ProUpRegTx) is used to update information relating to the owner. An owner can update the operator's BLS public key (e.g. to nominate a new operator), the voting address and their own payout address.  Dash Core allows us to run the following command if we want to update this information:

```
protx update_registrar <proTxHash> <operatorKeyAddr> <votingKeyAddr> <payoutAddress> <feeSourceAddress>
```

Where:
* proTxHash: The transaction id of the initial ProRegTx
* operatorKeyAddr: An updated BLS public key, or `""` to use the last on-chain operator key
* votingKeyAddr: An updated voting key address, or `""` to use the last on-chain voting key
* payoutAddress: An updated Dash address for owner payments, or `""` to use the last on-chain payout address
* feeSourceAddress: An address used to fund ProTx fee. Must have funds and the private key must be in your dash core wallet.

In order to update your information, you have to use the dash core wallet you used to generate your `ownerKeyAddr`, and it has to be unlocked.
