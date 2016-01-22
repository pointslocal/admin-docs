# /api/v1/showtimes

> API endpoint for movie times.  Times are grouped by theater.  Note: pagination and count parameters do not apply to this endpoint.  It will return all available showtimes and theaters for a given request.

##### Request Parameters
- **guid** ```string``` - Movie's GUID
- **movie_id** ```int``` - Movie's ID
- **venue_id** ```int``` - Theater's ID
- **date** ```string``` - Date for showtimes.  Accepts general, natural language dates
- **nearby** ```int``` - If set to 1 in combination with ```venue_id```, will return nearby theaters

##### Response Parameters
- **name** ```string``` - Theater name
- **address** ```string``` - Theater address
- **phone** ```string``` - Theater phone number
- **guid** ```string``` - Theater GUID
- **id** ```id``` - Theater ID
- **nearby** ```bool``` - If requested with nearby=1, will show true if the result is close to requested theater.  Exact theater requested will be set to false
- **movies** ```array```
    - **id** ```int``` - Movie ID
    - **title** ```string``` - Movie's full title
    - **guid** ```string``` - Movie's GUID
    - **date** ```string``` - Showtime date
    - **time** ```string``` - Showtime time
    - **new** ```bool``` - If movie's release date +/- one day from requested date
    - **times** ```array``` - Showtimes
    - **genres** ```string``` - Comma-separated list of genres
    - **qrating** ```float``` - Numerical quality rating (4-star scale; 0.0 - 4.0)
    - **stars_full** ```int``` - Number of full stars in quality rating
    - **stars_half** ```int``` - Number of half stars in quality rating
    - **stars_empty** ```int``` - Remainder of 4 - ```stars_full```+```stars_half```

> The values ```stars_full```, ```stars_half``` and ```stars_empty``` exist to allow simple templating languages to produce loops that generate 0-star to 4-star graphics. 

##### Useful ```sort_by``` Parameters
- **release_timestamp** - Will sort by the release date
- **rating** - Will sort by quality rating

## /api/v1/showtimes/[:id]
Requests showtimes by movie id
