# Pointslocal API

> The Pointslocal API is a RESTful API that drives a number of services including admin and widgets.

##### Request Parameters
- **api_key** ```string``` - Your application's API key.  This is required for some GET requests and all POST/PUT/DELETE requests
- **token** ```string``` - Paramaterized request token.  Not required if session ID is supplied.
- **date_format** ```string``` - An alternate date format.  Unless specified, dates will be returned in YYYY-MM-DD format
- **time_format** ```string``` - An alternate time format.  Unless specified, dates will be in 24:MM format
- **format** ```enum``` - Accepts ```xml``` or ```json``` with the latter being the default
- **count** ```int``` - Number of results per page to return
- **page** ```int``` - Page of results to return (index = page * count)
- **field_map** ```json``` - Allows you to change the response fields to match a schema.  As an example, if a response includes **title** in each item, you can replace that with **name** by supplying a URL-encoded field_map={"title":"name"} parameter.  The field map can also be set globally per publication under Admin :: Publications :: Settings

##### Response Parameters
- **items** ```array``` - All GET requests will return responses in an ```items``` array, even if only one record is impacted or requested