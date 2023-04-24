# Utils Route (/utils)
Utils Route's aim to list event with corresponding queries.

## [GET] /search?:searchTitle:id:page:pageLimit
The search endpoint returns pageLimit events that are in the page page with name searchTitle or with id id. It uses Mongodb find function and skips until the page with limit pageLimit.

## [GET] /get-events-by-category?:category
The /get-events-by-category?:category service's aim to find all events under category category by using MongoDb find function. Returns List of Events.