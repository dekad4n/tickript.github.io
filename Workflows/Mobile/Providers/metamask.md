# Metamask Provider

## Why we used such provider?
We wanted to centralize all metamask actions and the loginning to metamask system.

## Variables

### _uri
It is a string variable which corresponds to chain's uri.

### _session
Current active session of Metamask login. default: null.

### currentAddress
Connected user's public address, string. default: empty string

### chainId
Constant value equals to 80001 (Mumbai Testnet chain id)

### connector
WalletConnect classed connector with meta variables

## Functions

### loginUsingMetamask
If the connector is not connected, it creates new session with .createSession function of connector. Then, chainId, currentAddress and _session is updated with respect to session's value. Then it notifies all listeners of the provider to update with notifyListeners() function of flutter:provider package.

### sign
Used to get sign with respect to nonce. Creates list of strings to give sendCustomRequest function. Firstly, it calls launchUrl with converting session's uri with uri parse, then sends custom request with connector's sendCustomRequest function

### logout
If connector is connected, kills session of connector and erases datas of variables. Then notifies listeners of Metamask Provider

### clear
Clears all variables and notifies listeners.

### init
Binds SessionUpdate and Disconnect functions of connector to clear data with clear function.


## Where it is used?
It is used in wrapper of the app, therefore **all the components** of the app listens Metamask Provider.