# Auction Route (/auction)
The Auction Route's aim to handle auction data or get data about tickets/events that is related with auction mechanism.

## [GET] /auctions-by-event-id?:eventId
The /auctions-by-event-id?:eventId finds all auctions under the event with id eventId with calling GetAuctionInfo function of our Auction Contract. It returns list of auctions.

## [POST] /create-bid-item
The /create-bid-item service's aim to prepare data to create a bid item (start auction). It takes ticketId, eventId, startPrice, time and prepares transactionParameters with createBidItem function of our contract.

## [POST] /stop-auction
The /stop-auction service's aim to prepare data to stop auction with id auctionId. It encodes data with StopAuction function of our Auction Contract.

## [GET] /get-auction
The /get-auction?:auctionId returns auction data of auction with id auctionId by calling GetAuctionInfo function of our Auction Contract.

## [GET] /list-prev-bids?:auctionId
The /list-prev-bids?:auctionId returns previous bids that belongs to auction with id auctionId by calling listPrevBids method of our Auction Contract.

## [POST] /bid
The /bid service's aim to prepare data for bidding to an bidding item with auctionId. It also takes bidPrice to encode with placeBid function of our Auction Contract and returns encoded data to user.

## [POST] /finish-bid
The /finish-bid service's aim to prepare data for ending auction with id auctionId with encoding data with finishBid function of our Auction Contract.

## [POST] /payback-prev-bids
The /payback-prev-bids service's aim to prepare data for refunding old bids that belongs to auctionId by encoding the data with payBackPrevBids function of our Auction Contract.

