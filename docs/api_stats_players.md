# /api/v1/players
### GET

##### Request Parameters
- search **[ string ]** - Freeform search text, matches player's name or school
- position **[ string ]** - Filters by position GUID
- active_year **[ int ]** - Active year
- grad_year **[ int ]** - Graduation year of player
- guid **[ string ]** - Player's GUID

##### Response Parameters
- guid **[ string ]** - Player's GUID
- name **[ string ]** - Player's full name
- firstname **[ string ]** - Player's first name
- lastname **[ string ]** - Player's last name
- schools **[ array ]** - Schools to which player belongs
- meta **[ array ]** - An array of player metadata
- sports **[ array ]** - List of sports the player is connected

##### Example Response
``` json
[
    {
        "counter": 0,
        "guid": "170",
        "sport_id": "0",
        "name": "John Doe",
        "firstname": "",
        "lastname": "",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 1,
        "guid": "224",
        "sport_id": "0",
        "name": "John Pochebit",
        "firstname": "John",
        "lastname": "Pochebit",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 2,
        "guid": "231",
        "sport_id": "0",
        "name": "John Watson",
        "firstname": "John",
        "lastname": "Watson",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 3,
        "guid": "232",
        "sport_id": "0",
        "name": "John Fournel",
        "firstname": "John",
        "lastname": "Fournel",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 4,
        "guid": "258",
        "sport_id": "0",
        "name": "John Boucher",
        "firstname": "John",
        "lastname": "Boucher",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 5,
        "guid": "295",
        "sport_id": "0",
        "name": "John Forrestell",
        "firstname": "John",
        "lastname": "Forrestell",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 6,
        "guid": "307",
        "sport_id": "0",
        "name": "John Asdourian",
        "firstname": "John",
        "lastname": "Asdourian",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 7,
        "guid": "335",
        "sport_id": "0",
        "name": "John McDonough",
        "firstname": "John",
        "lastname": "McDonough",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 8,
        "guid": "342",
        "sport_id": "0",
        "name": "John Groder",
        "firstname": "John",
        "lastname": "Groder",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    },
    {
        "counter": 9,
        "guid": "361",
        "sport_id": "0",
        "name": "Brandon Kyajohnian",
        "firstname": "Brandon",
        "lastname": "Kyajohnian",
        "grad_year": "",
        "meta": [

        ],
        "sports": [

        ],
        "schools": [

        ]
    }
]
```