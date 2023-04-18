# Authentication Middleware
Tickript's authentication system in the Tickript's backend services are based on the Authentication Middleware. As [General Authentication](/Workflows/General/Authentication.md) explains, the backend's authentication is handled with Json Web Tokens (JWTs).

In every service that needs authentication calls Authentication Middleware before it proceeds any other work. 

The Authentication Middleware takes the token that is sent with header Authorization. Then, it proceeds sent token and checks whose token is sent. It finds it the database whose token it is and adds user's information to request according to [User Modal](/Modals/user.md). 