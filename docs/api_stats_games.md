# /api/v1/games

##### Request Parameters
- **date** ```string``` - Return games by date in a flexible format, though it's recommended you use MM/DD/YYYY.  It also accepts relative strings like "tomorrow" or "today".  In addition, it will accept some fuzzy options like "today-recent", which allows you to show the most recent scores +/- 1 day unless there are games scheduled for today.  This is useful for the scoreboard widget.

##### Response Parameters
- **guid** ``` string``` - Games internal GUID
- **game_id** ``` int``` - Integer ID of game, for requesting games by ID
- **away_nickname** ```string``` - Away team's nickname
- **away_name** ```string``` - Away team's name / school name
- **home_nickname** ```string``` - Home team's nickname
- **home_name** ```string``` - Home team's name / school name
- **winner_name** ```string``` - Winning team's name
- **winner_score** ```int``` - Winning team's score
- **losing_name** ```string``` - Losing team's name
- **losing_score** ```int``` - Losing team's score

## /api/v1/games/[:id]
Requests a specific game

##### Response Parameters For Individual Games
- **plays** ```array``` - List of individual plays/scoring plays
- **home_periods** ```array``` - List of active periods for home team
- **away_periods** ```array``` - List of active periods for away team