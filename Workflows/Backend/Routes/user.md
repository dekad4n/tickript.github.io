# User Route (/user)
User Route's aim to handle requests that is related to an user's profile provided with corrsponding public address.

## [GET] /:publicAddress
The /:publicAddress endpoint's aim is to create an user with corresponding public address if user does not exists with that address or return the user if the user exists.

## [POST] /update
The /update service's aim is to update user profile that comes from [Authentication Middleware](/Workflows/Backend/Middlewares/Authentication.md). It updates avatar, name and username of the user in MongoDb.

## [GET] /events?:publicAddress
The /events?:publicAddress service's aim to get every event that is belonged to publicAddress from MongoDb.

## [GET] /tickets?:publicAddress
The /tickets?:publicAddress service's aim to get tickets that is belonged to publicAddress from the chain. It calls ListEventTicketByPublicAddress function of our contract and maps it with our MongoDb [Event Modal](/Modals/event.md).


