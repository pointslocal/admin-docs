# /api/v1/neighborhoods

> API endpoint for requesting geographic information.  Please note that all geographic entities are "neighborhoods," irrespective of actual administrative type or hierarchy.

##### Request Parameters
- **guid** ```string``` - Neighborhood's GUID
- **search** ```string``` - Text string that matches neigborhood names
- **latitude** ```float``` - When paired with longitude, returns neighborhoods that contain the lat/lon point
- **longitude** ```float``` - When paired with latitude, returns neighborhoods that contain the lat/lon point
- **radius** ```float``` - When paired with latitude and longitude, returns neighborhods that are within the requested area
- **suppress_geo** ```int``` - When set to 1, results will not include polygon data.  Default: 0
- **ids** ```string``` - A comma separated list of neighborhood IDs

##### Response Parameters
- **id** ```string``` - Neighborhood's ID
- **name** ```string``` - Neighborhood name
- **guid** ```string``` - Neighborhood's GUID
- **neighborhood_poly** ```array``` - Returns a list of longitude/latitude points

## /api/v1/neighborhoods/[:id]
Requests a specific neighborhood
