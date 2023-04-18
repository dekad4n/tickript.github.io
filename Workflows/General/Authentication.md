# Authentication Mechanism
Our authentication mechanism has 2 parts: Authentication with Metamask and Authentication with JWT token. 

## Authentication with Metamask
In the mobile part, we have created login button. Whenever a user clicks onto login button, we open Metamask with [WalletConnect API](https://docs.walletconnect.com/2.0). If user permits logging in, the user will pass to JWT Authorization part.

## JWT Authorization
Our JWT Authorization is based on the backend. When a user is logged into Metamask, the [User Provider](/Workflows/Mobile/Providers/user.md) forces user to sign a Metamask request. Then, we send signature and nonce of the user to backend, and verify if the user is the authorized user. Backend responds with a JWT token, which is deposited in the [User Provider](/Workflows/Mobile/Providers/user.md) of the mobile part.

If a backend service needs authentication, we send following code part in the header:
```
Authorization = "jwt ${JWT}"
```

That is how we handle Authorization via our backend services.