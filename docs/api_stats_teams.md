# /api/v1/teams

##### Request Parameters
- **sport** ``` string ``` - Requested sport
- **division** ``` string ``` - Requested division

##### Response Parameters
- **teams** ``` array ``` - An array of team objects (name, guid) sorted by sport-specific formula

## /api/v1/teams/[:id]
Requests a specific team