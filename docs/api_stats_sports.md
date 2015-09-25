# /api/v1/sports
### GET

##### Request Parameters
- search **[ string ]** - Freeform search text, matches sport name
- season **[ enum ]** - Accepts (winter, spring, summer, fall)

##### Response Parameters
- guid **[ string ]** - Sport's internal GUID
- name **[ string ]** - Sport's name
- seasons **[ array ]** - List of applicable seasons