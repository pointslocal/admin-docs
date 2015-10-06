# /api/v1/stories

> API endpoint for requesting aggregated or created stories.

##### Request Parameters
- guid ```string``` - Requests story by GUID
- date ```string``` - Story's date
- range ```string``` - A range of dates; returns stories published in this timeframe
- search ```string``` - Searches title and text for requested string
- source_id ```int``` - Returns stories only from this source, as returned by /api/v1/sources


##### Response Parameters
- title ```string``` - Event's title
- description ```string``` - Full description for event.
- text ```string``` - Fulltext of story
- image_id ```int``` - If available, the primary image ID for the story
- date ```string``` - Story's date in requested or default format ([see main API options](api.md))
- time ```string``` - Story's time in requested or default format ([see main API options](api.md))

## /api/v1/stories/[:id]
Requests a specific story
