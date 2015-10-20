# /api/v1/movies

> API endpoint for movies.

##### Request Parameters
- **guid** ```string``` - Event date's GUID.  This is a reference to an individual recursion's GUID, not the overall event


##### Response Parameters
- **id** ```int``` - Internal ID
- **title** ```string``` - Movie's full title
- **guid** ```string``` - Movie's GUID
- **description** ```string``` - Movie's full description
- **short** ```string``` - Short description
- **url** ```string``` - Movie's URL
- **language** ```string``` - Spoken language for movie
- **runtime** ```int``` - Movie's runtime, in seconds
- **qrating** ```float``` - Movie's TMS rating, from 0 to 4


## /api/v1/movies/[:id]
Requests a specific movie
