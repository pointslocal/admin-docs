# /api/v1/showtimes

> API endpoint for movie times.

##### Request Parameters
- **guid** ```string``` - Movie's GUID
- **movie_id** ```int``` - Movie's ID
- **theater_id** ```int``` - Theater's ID
- **date** ```string``` - Date for showtimes.  Accepts general, natural language dates

##### Response Parameters
- **id** ```int``` - Movie ID
- **title** ```string``` - Movie's full title
- **guid** ```string``` - Movie's GUID
- **venue_name** ```string``` - Name of venue/theater
- **venue_name** ```string``` - Name of venue/theater
- **venue_id** ```int``` - Venue/theater's internal ID
- **venue_guid** ```string``` - GUID for venue/theater
- **date** ```string``` - Showtime date
- **time** ```string``` - Showtime time

## /api/v1/showtimes/[:id]
Requests showtimes by movie id
