# /api/v1/standings
> The standings API endpoint produces automated total and in-division standings for teams by requested division and season.  A season contains a combination of sport and timeframe; this endpoint calculates wins, losses and other information about teams compared to in-division competition within a season.  It's important to note that incomplete data (lack of scores, for example) will result in this data subsequently also being incorrect. As such, this (and the standings widget) are best utilized in cases where complete data exists for teams within a division.

##### Request Parameters
- **season** ```string``` - Requested season GUID
- **division** ```string``` - Requested division

##### Response Parameters
- **items** ```array``` - An array of team objects (name, guid) sorted by sport-specific formula
    - **id** ```int``` - Team ID
    - **guid** ```string``` - Team's GUID
    - **nickname** ```string``` - Team nickname/mascot (if available)
    - **name** ```string``` - School or team name
    - **has:image** ```bool``` - True if team has an image associated with it
    - **wins** ```int``` - Team's overall wins for season
    - **losses** ```int``` - Team's overall losses for season
    - **pct** ```float``` - Team's winning percentage to 3 decimal places
    - **conference_wins** ```int``` - Team's conference wins
    - **conference_losses** ```int``` - Losses in conference games
    - **conference_pct** ```float``` - Conference winning percentage
    - **games_back** ```float``` - Number of games behind (wins + #1 losses) from first place
    - **streak** ```string``` - Formatted ```W#``` or ```L#```
    - **ppg** ```float``` - Average score per game
    - **pf** ```int``` - Number of "points" scored
    - **pa** ```int``` - Number of "points" scored against

## /api/v1/standings/[:id]
Requests a specific standing by *team* ID, returning that team's divsion/conference