# Sports Variables


### Export Template Variables
To read more about the export process, read <a href="/events_exports/">Events Exports</a>

#### Group Variables - Games

The **games** variable holds an array of **items**

#### Game Item Variables
  - **title** ```string``` Game title (if available)
  - **teams** ```array``` All participating teams (see below, team items)
  - **home** ```array``` The home team (if applicable)
  - **away** ```array``` The away team (if applicable)
  - **print_title** ```string``` If a print title exists, its value will be output with this variable.
  - **custom** ```array``` Array of custom values

#### Team Item Variables
  - **record** ```array``` Wins, losses and ties
  - **conference_record** ```array``` Wins, losses and ties within conference
  - **score** ```int``` Final tally
  - **periods** ```array``` Score by period
  - **players** ```array``` Teamm's players (see below, player items)