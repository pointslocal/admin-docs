# /api/v1/standings

##### Request Parameters
- **sport** ``` string ``` - Requested sport
- **division** ``` string ``` - Requested division

##### Response Parameters
- **teams** ``` array ``` - An array of team objects (name, guid) sorted by sport-specific formula

## /api/v1/standings/[:id]
Requests a specific standing