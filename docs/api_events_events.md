# /api/v1/events

> API endpoint for requesting events, returning only events which have a date associated with them.  Images URLs can be created utilizing the [image construction documentation](images.md) using the context ```event.image```.  If using stock art with categories, calling images with the context ```event.yield``` will first attempt to return an event's image and if none is found will then return category stock art.  As with any data type that supports multiple images, the events endpoint will also accept an ```any``` request, which will a random selection from the event's images.  This is invoked with ```event.any```.

> The ```event.yield``` uses the following passthru logic:

* Event has image, else
* Event venue has an image, else
* Event category has an image

In addition to the ```event.yield``` context, calling ```event.yield.neighbors``` will show the image of the closet event (in terms of time) that has an image from the same venue.

##### Request Parameters
- **search** ```string``` - Freeform search text, which will match against title, description and venue
- **guid** ```string``` - Event date's GUID.  This is a reference to an individual recursion's GUID, not the overall event
- **start** ```string``` - Event start date
- **end** ```string``` - Event end date.  Completes start <-> end range
- **date** ```string``` - Event's date
- **range** ```string``` - Start and end dates separated by '-'.  Example: 20010101-20010102
- **when** ```string``` - Accepts natural language relative dates like ```this week``` or ```next month```
- **category** ```string``` - Returns events in category by category GUID [See category API](api_events_categories.md)
- **category_id** ```int``` - Returns events from this category. [See category API](api_events_categories.md)
- **featured** ```int``` - Returns currently featured events if set to 1. Default: 0
- **popular** ```int``` - Returns the most popular events if set to 1.  Default: 0 *Note: setting this to 1 implicitly sorts results by popularity in descending order*
- **popcategory** ```int``` - Selects only popular events from this category
- **popdays** ```int``` - Number of days back to look for popular events.  Default: 1, Maximum: 14
- **venue_guid** ```int``` - Returns events from a specified venue
- **tag** ```string``` - Returns events with specified tag
- **published** ```int``` - Returns events that are published by default or with value 1.  If set to 0 will display unpublished.  Default: 1
- **latitude** ```float``` - Searches within longitude/latitude if paired radius
- **longitude** ```float``` - Searches within longitude/latitude if paired with radius
- **radius** ```float``` - A radius (in miles) that, when paired with latitude and longitude, returns results in a medium bounding rectangle
- **neighborhood_id** ```int``` - Restricts results to spatial containment of given neighborhood.  [See neighborhood API](api_places_neighborhoods.md)
- **movie** ```int``` - If set to 1, returns movie results
- **parent_id** ```int``` - The parent event for all recurrences
- **recurrences** ```int``` - Returns future recurrences of event.  Note: this can slow down requests if an event has many recurrences

##### Response Parameters
- **title** ```string``` - Event's title
- **description** ```string``` - Full description for event
- **print_description** ```string``` - Print description if available.  Will return **description** if null or empty
- **address** ```string``` - Event's address
- **latitude** ```float``` - Event's latitude
- **longitude** ```float``` - Event's longitude
- **id** ```int``` - Internal numerical ID
- **parent_id** ```int``` - Event recurrence's parent ID.
- **guid** ```string``` - Event's GUID
- **has_image** ```bool``` - True if event has image associated with it
- **image_id** ```int``` - Event image ID
- **date** ```string``` - Event date in requested or default format ([see main API options](api.md))
- **start_time** ```timestamp``` - Event's start time in requested or default format ([see main API options](api.md))
- **end_time** ```timestamp``` - Event's end time in requested or default format ([see main API options](api.md))
- **url** ```string``` - Event's URL
- **phone** ```string``` - Event's phone
- **venue_id** ```int``` - Event's venue ID
- **venue_guid** ```string``` - Event's venue GUID
- **venue_name** ```string``` - Event's venue
- **venue_address** ```string``` - Event's venue address.  This may be the same as ```address``` unless it is overridden for the event
- **recurrences** ```array``` - A list of future recurrences, if requested with recurrences=1
- **category_id** ```int``` - Event's *primary* category
- **categories** ```array``` - A list of other associated categories
- **tags** ```array``` - A list of tags associated with event
- **movie_guid** ```string``` - If ```movie=1``` is set, will return internal GUID of movie
- **movie_id** ```int``` - If ```movie=1``` is set, will return numerical ID of movie ([see movie API options](api_events_movies.md))

## /api/v1/events/[:id]
Requests a specific event
