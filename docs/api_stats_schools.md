# /api/v1/schools
### GET

##### Request Parameters
- search **[ string ]** - Freeform search text matches school name or mascot
- division **[ string ]** - Schools by division GUID

##### Response Parameters
- school **[ string ]** - Name of school itself
- mascot **[ string ]** - Mascot name (if available)
- teams **[ array ]** - An array of all available teams per school
- meta **[ array ]** - An array of all supplied metadata fields