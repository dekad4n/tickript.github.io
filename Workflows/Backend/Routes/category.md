# Category Route (/category)
Since categories are not changable by end-users, category services only consist getters for ordinary users. However an admin of Tickript can add an category. Other than that category services are not in touch with any contract methods.

## [GET] /get-all 
The /get-all service of category route gets all categories from the MongoDb Atlas database and returns them to the requesting user.

## [POST] /add 
The /add service is called by Tickript admins and takes 2 inputs at it's body according to [Category Modal](/Modals/category.md): image and name. After validating the inputs, it adds the category into MongoDb Atlas Database. 