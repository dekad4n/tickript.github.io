# Transactions
To prevent repeated explanations in the document, this part will explain how Tickript handles the transaction in the general structure.

Every transaction starts at the mobile application. The mobile application collects necessary inputs from the user to call the corresponding backend service. Then, it requests to backend service with correct format.

After that, backend service responses to mobile app with 2 different statements:
- Valid
- Error

Backend always encodes the datas with encodeABI() function of the contract, however, depending on the inputs the state changes.

If the inputs are valid and transaction is available to do, backend service sends following data structure to user:
```
transactionParameters = {
    from: {THE_ADDRESS_OF_USER},
    to: {CORRESPONDING_CONTRACT_ADDRESS},
    data: {DATA_THAT_COMES_FROM_ENCODE_ABI},
    value: {VALUE_OF_TRANSACTION} # optional
}
```

The mobile application gains the transactionParameter and sends it to chain via using alchemy.sendTransaction() function. If the signature of user is needed, it is handled via [Metamask Provider](/Workflows/Mobile/Providers/metamask.md). 