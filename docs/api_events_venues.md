# /api/v1/venues

##### Request Parameters
- search ```string``` - Text string for search.  Will match venue name unless search_all is set, in which case it will match name, address, description and reviews.
- search_all ```bool``` - Modifies search fields for search parameter.
- latitude ```float``` - Latitude for geo search
- longitude ```float``` - Longitude for geo search
- radius ```float``` - Range for geo search, in miles
- rating ```string``` - A range for ratings.  "0,5" would show venues with a rating less than or equal to 5.0
- approved ```int``` - Set to 1 to return only approved venues. Default: 0
- theater ```bool``` - If set to true or 1, will return venues that are listed as movie theaters

##### Response Parameters
- guid ```string``` - Internal GUID for this venue
- name ```string```
- address ```string```
- url ```string``` - Web site, if available
- price ```int``` - Numerical representation of price from 1-4 (often expressed $, $$, $$$, $$$$)
- rating ```float``` - Average rating for venue, from 0.0 to 10.0
- reviews ```array``` - List of community reviews and ratings
- approved ```bool``` - True if venue is approved
- theater ```bool``` - True if venue is set as movie theater

## /api/v1/venues/[:id]
Requests details on a specific venue