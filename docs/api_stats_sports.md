# /api/v1/sports

##### Request Parameters
- **search** ```string``` - Freeform search text, matches sport name
- **season** ```enum``` - Accepts (winter, spring, summer, fall)

##### Response Parameters
- **guid** ```string``` - Sport's internal GUID
- **name** ```string``` - Sport's name
- **seasons** ```array``` - List of applicable seasons

## /api/v1/sports/[:id]
Requests a specific sport
