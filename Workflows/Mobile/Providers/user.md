# User Provider
User Provider is used to login into backend after [Metamask Provider](/Workflows/Mobile/Providers/metamask.md) done loginWithMetamask. It wraps all the components except Metamask Provider in the wrapper component.

## Variables

### token
Token is a nullable string which is the JWT token of the user. Empty string if default.

### user
User classed object which contains user's data

## Functions

### hasToken
Checks if token is defined.

### handleLogin
If token is not defined, takes currentAddress from Metamask Provider, gets nonce from the backend, signs the nonce and calls login path of the backend. Gets token from the result and notifies all components under it.

### handleUpdate
If metamask provider is changed, gets the current nonce and notifies its listeners.

