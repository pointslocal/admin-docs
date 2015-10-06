# /api/v1/events

> API endpoint for requesting events, returning only events which have a date associated with them.

##### Request Parameters
- guid ```string``` - Event date's GUID.  This is a reference to an individual recursion's GUID, not the overall event
- start ```string``` - Event start date
- end ```string``` - Event end date.  Completes start <-> end range.
- date ```string``` - Event's date
- range ```string``` - Start and end dates separated by '-'.  Example: 20010101-20010102
- category ```string``` - Returns events in category by category GUID
- featured ```int``` - Returns currently featured events if set to 1. Default: 0
- venue_guid ```int``` - Returns events from a specified venue


##### Response Parameters
- title ```string``` - Event's title
- description ```string``` - Full description for event.
- print_description ```string``` - Print description if available.  Will return **description** if null or empty.
- guid ```string``` - Event's GUID
- image_id ```int``` - Event image ID
- date ```string``` - Event date in requested or default format ([see main API options](api.md))
- start_time ```timestamp``` - Event's start time in requested or default format ([see main API options](api.md))
- end_time ```timestamp``` - Event's end time in requested or default format ([see main API options](api.md))
- venue_id ```int``` - Event's venue ID

## /api/v1/events/[:id]
Requests a specific event
