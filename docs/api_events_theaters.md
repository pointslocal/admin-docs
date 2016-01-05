# /api/v1/theaters

> API endpoint for theaters.

##### Request Parameters
- **near** ```string``` - A coordinate in lat,lon format.


##### Response Parameters
- **id** ```int``` - Internal ID
- **guid** ```int``` - Internal GUID
- **name** ```string``` - Name of theater
- **address** ```string``` - Theater's address
- **latitude** ```float``` - Theater's latitude
- **longitude** ```float``` - Theater's longitude
- **phone** ```string``` - Theater's phone number

## /api/v1/theaters/[:id]
Requests a specific theater
