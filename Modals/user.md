# User Modal
Our user modal is used when a user logins with Metamask. Since we wanted to customize our users, we created such modal. The fields of user model will be described below.

## publicAddress
publicAddress is a required string field. It is user's public wallet address.

## name
name is a string field. Once an user logs in, the default name of the user is its public address. However, an user can change its name.

## username
name is a string field. Once an user logs in, the default username of the user is its public address. However, an user can change its username.

## nonce
nonce is a string field. It is set when user is created by uuid.v4() algorithm. We use that to authenticate user sometimes.

## avatar
avatar is a string field. It provides user's profile picture in terms of URLs.


