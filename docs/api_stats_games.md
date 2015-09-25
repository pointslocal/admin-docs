# /api/v1/games

##### Request Parameters
- date **[ string ]** - Return games by date in a flexible format, though it's recommended you use MM/DD/YYYY.  It also accepts relative strings like "tomorrow" or "today".  In addition, it will accept some fuzzy options like "today-recent", which allows you to show the most recent scores +/- 1 day unless there are games scheduled for today.  This is useful for the scoreboard widget.

##### Response Parameters
- guid **[ string ]** - Games internal GUID
- game_id ** [ int ]** - Integer ID of game, for requesting games by ID

## /api/v1/games/[:id]
Requests a specific game