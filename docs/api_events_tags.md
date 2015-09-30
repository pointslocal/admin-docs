# /api/v1/tags

##### Request Parameters
- guid ```string``` - Tag ontology
- parent ```int``` - ID for parent tag, returns children


##### Response Parameters
- guid ```string``` - Tag's GUID
- id ```int``` - Tag's ID
- parent_id ```int``` - Tag's parent
- parent_term ```string``` - Tag's parent tag

## /api/v1/tags/[:id]
Requests details on a specific venue