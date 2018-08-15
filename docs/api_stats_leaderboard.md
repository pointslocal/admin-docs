# /api/v1/leaderboard
> Returns the top performing players for a given day by a set of statistical attributes.

##### Request Parameters
- **leaders** ``` string ``` - A pipe-delimited set of stat groups in the form ```statguid:minimum:count|statguid2:minimum:count```.
- **date** ``` string ``` - Select by a specific date. Default: today.


##### Response Parameters
- **groups** ``` array ``` - The requested stats containing a the ```leaders``` array.
- **groups[n].label** ```string``` - The statistical group's name.
- **groups[n].leaders** ``` array ``` - An array of matching players.
- **groups[n].leaders[n].name** ``` string ``` - The player's name.
- **groups[n].leaders[n].value** ``` int ``` - The player's stat value.


### Example Request
```[site]/api/v1/leaderboard?leaders=passing:200:10|rushing:100:5|receiving:100:5```

Where passing is the guid for Passing yards with a minimum of 200, rushing for Rushing yards with a minimum of 100 and receiving for Receiving yards with a minimum of 100.

Returns the top 10 passers, top 5 rushers and receivers.