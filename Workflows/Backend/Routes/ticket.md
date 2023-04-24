# Ticket Route (/ticket)
Ticket Route is implemented to work on tasks that are **mainly** related to tickets. The Ticker Route does not use any specific modal, therefore, one may have little understanding during the documentation.

## [GET] /:id
The /:id service's aim to get metadata of the ticket with tokenId id. It uses Alchemy's getNftMetadata function to provide requested ticket to the user.

## [POST] /mint
The /mint service's aim to prepare transaction paramaters for the mint transaction done in frontend. After input validations, it pins image to IPFS. Then, it pins other metadata with ipfs link again to IPFS. Then, with an IPFS link, it prepares the transasction data by calling encodeABI function of our Mint Contract.

## [POST] /is-ticket-checked
The /is-ticket-checked service's aim to give ticket's controller state to the controller. Firstly, it is an authenticated service. After authentication, it calls NFTItem function of our Market Contract, and looks at used value. If ticket is used, it returns true. Then, it checks if user is really a controller (authenticated one). If yes, it checks if QR code creator is the ticket owner by recovering personel signature from nonce and signature. If yes, it tries to find if the ticket is checked, if yes, it returns true, if no adds to database and returns true.

## [POST] /change-ticket-used-state
The /change-ticket-used-state service's aim to change tokens' usage value that is checked by caller and belongs to eventID to true. It returns data of encoded given values as transactionParameters.

