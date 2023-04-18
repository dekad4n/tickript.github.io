# Event Route (/event)
Event Route is created to handle get, put, post and delete operations that are related to Events. Event Route uses both contract and MongoDb methods in it.

# [GET] /:id
The /:id service of the Event Route returns the [Event Modal](/Modals/event.md) that corresponds to queried id. After validating the query, it finds the event by id in the MongoDb Atlas Database and returns it to requesting user.

# [GET] /get-random-event
The /get-random-event service of the Event Route returns the [Event Modal](/Modals/event.md) which is a random event. It returns a single random event to requesting user.

# [GET] /minted-event-ticket-tokens?:integerId
The /minted-event-ticket-tokens service of the Event Route returns the Tickets that are created under given integerId of the Event. It calls .getEventTicketList method of our contract and returns the list of tickets under the event to requesting user.

# [POST] /create
The /create service of the Event route creates a new Event according to [Event Modal](/Modals/event.md). It requires authentication. After validating authentication and inputs, it creates a new event in the MongoDb Atlas Database

# [POST] /set-ticket-controller
The /set-ticket-controller service of the Event Route returns a transaction data to add new ticket controller to the event. It encodes the given publicAddress and eventID with our Minting Contract and returns transaction parameters as stated in [Transactions](/Workflows/General/Transactions.md). It requires authentication.

# [POST] /is-ticket-controller
The /is-ticket-controller service of the Event Route returns if the one is a ticket controller for corresponding event. It requires authentication. By calling our verifyTicketController method of Mint Contract, it checks if user with publicAddress is an Event Controller for the event with eventID.

