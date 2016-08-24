# /api/v1/games

##### Request Parameters
- **range** ```string``` - In the format 01/02/2003-01/03/2003, will return games that were or are played within the specified range
- **date** ```string``` - Return games by date in a flexible format, though it's recommended you use MM/DD/YYYY.  It also accepts relative strings like "tomorrow" or "today".  In addition, it will accept some fuzzy options like "today-recent", which allows you to show the most recent scores +/- 1 day unless there are games scheduled for today.  This is useful for the scoreboard widget.  Setting to ```upcoming``` will just limit to future events without an end date.
- **season** ```string``` - A season GUID, will combine ```sport``` and ```range``` into a single request
- **sport** ```string``` - A sport's GUID
- **team** ```string``` - A team's GUID
- **class** ```string``` - A class GUID, will return results for teams or schools in a class
- **division** ```string``` - A division GUID, will return results for teams in a division


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
- **teams** ```array``` - A list of participating teams
	- **name** ```string``` - The team's name
	- **guid** ```string``` - The team's GUID
	- **abbreviation** ```string``` - The team's abbreviation
	- **score** ```int``` - Final score for team
	- **periods** ```array``` - A list of periods for the team
	- **players** ```array``` - A list of players & corresponding individual stats for team

- **sports** ```array``` - Groups all of the games under their respective sport.

## /api/v1/games/[:id]
Requests a specific game

##### Response Parameters For Individual Games
- **plays** ```array``` - List of individual plays/scoring plays
- **home_periods** ```array``` - List of active periods for home team
- **away_periods** ```array``` - List of active periods for away team