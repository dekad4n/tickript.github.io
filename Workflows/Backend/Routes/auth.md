# Authentication Route (/auth)

Authentication Service's aim is to provide a login system. It has only 1 useful endpoint called /login.

## /login
The login endpoint has 2 paths: 
- User is already signed up
- User that did not signed up

With looking session value of user, /login method decides the signed-up state of the user. If the user is signed up, it generates a JWT token and calls our contract's verifyEventOwner method to see if user is whitelisted. Then, it sends both information to user.

If user is not signed up, it requires 2 parameters: nonce and signature. Then, using nonce and signature, it re-generates user's public address and adds a user with that public address and nonce to MongoDb Atlas Database. After that, it verifies if user is whitelisted already. Then, it returns User Modal and whitelist information to the requesting user.