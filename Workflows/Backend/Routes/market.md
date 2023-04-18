# Market Route (/market)
Market route is specifically created to work with Market Contract.

## [GET] /market-item?:tokenId
The /market-item service of the Market Route gets the item that is an element market contract by using tokenId query parameter via calling NFTItem method of our Market Contract. It returns data of that token to the requesting user.

## [GET] /market-items-all?:eventId
The /market-items-all service of the Market Route gets all the tickets which is in Market Block and has the eventId. It gets them via calling ListEventTicketAll method of our Market Contract and returns list of tickets to the requesting user.

## [GET] /transferable-ids?:eventId&:publicAddress
The /transferable-ids service of the Market Route return all the tickets that is transferrable under eventId and owned by publicAddress. It gets them via calling TransferableIds method of our MarketContract and returns them to requesting user.

## [POST] /transfer
The /transfer service of the Market Route returns data for the Transfer transaction according to [Transactions](/Workflows/General/Transactions.md). It gets tokenId and a toAddr, which means which user you want to send the ticket, and returns transaction data by encoding with TransferTicket method of our Market Contract.

## [POST] /resell
The /resell service of the Market Route returns data for the Resell transaction according to[Transactions](/Workflows/General/Transactions.md). It gets tokenId and a price, returns transaction data by encoding with ResellTicket method of our Market Contract. Resell means selling a ticket at second or more time.

## [POST] /sell
The /sell service of the Market Route returns data for the Sell transaction according to[Transactions](/Workflows/General/Transactions.md). It gets price, eventId, amount and transactionRight returns tra transaction data by encoding with createMarketItem method of our Market Contract. It is called when a ticket will be sold first time.

## [POST] /stop-sale
The /stop-sale service of the Market Route returns data for the Stop Sale transaction according to[Transactions](/Workflows/General/Transactions.md). It gets tokenId and a price, returns transaction data by encoding with StopTicketSale method of our Market Contract. It is called to stop sale of a single item.

## [POST] /stop-batch-sale
The /stop-batch-sale service of the Market Route returns data for the Stop Batch Sale transaction according to[Transactions](/Workflows/General/Transactions.md). It gets tokenIds, eventId and a price, returns transaction data by encoding with StopBatchSale method of our Market Contract. It is called to stop sale of all tokenIds under the event with eventId.

## [POST] /buy
The /buy service of the Market Route returns data for the Buy transaction according to[Transactions](/Workflows/General/Transactions.md). It gets tokenIds and a price, returns transaction data by encoding with ticketSale method of our Market Contract. It is called to buy tickets with tokenIds with the corresponding price.
