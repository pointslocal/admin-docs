# /api/v1/events/[:id]/dates

> This endpoint returns all recurrences for a given event ID, as returned by the ```/api/v1/events``` endpoint

##### Request Parameters
- **id** ```int``` - The event date's ID, which will return sibling recurrences

##### Response Parameters
- **date** ```string``` - Event date in requested or default format ([see main API options](api.md))
- **start_time** ```timestamp``` - Event's start time in requested or default format ([see main API options](api.md))
- **end_time** ```timestamp``` - Event's end time in requested or default format ([see main API options](api.md))