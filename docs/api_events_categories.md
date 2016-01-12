# /api/v1/event_categories

##### Request Parameters
- **search** ```string``` - Text string for search, matching category's name

##### Response Parameters
- **id** ```int``` - Internal ID for category
- **guid** ```string``` - Internal GUID for this category
- **name** ```string```
- **parent_id** ```int``` - Parent category id

## /api/v1/event_categories/[:id]
Requests a specific category and details