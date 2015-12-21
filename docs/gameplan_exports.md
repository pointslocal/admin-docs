![Gameplan](img/gameplan_logo.png)

# Exporting For Print
> This guide will explain the sports-specific print export options for Gameplan agate, stats, schedules and standings. To read more about the export process, please see <a href="/events_exports/">Events Exports</a>

### Config - Generators
> Generators offer a chance to create a computed stat or metric based on one or more qualifiers.  The initial use case was for computing when a player has been fouled out in basketball after accruing five personal fouls (or more, in edge cases).

In the above example, we'll assume we have an individual statistic called Personal Fouls (with an abbreviation of PF).  Since we want to operate on this value, we can then check if each player's corresponding value is below, meets or exceeds a given value.

```javascript
"generators":[
{"type":"computedLinescore","options":[{"field":"PF","minValue": 5, "newField":"fouled_out", "value": true }]}
]
```

On export, each player's linescores will be evaluated; if an individual player has a PF value at or above 5 (the ```minValue```), a new stat field will be added called "fouled_out".  This will be accessible in the template as ```stat_fouled_out``` in the linescores loop.

```javascript
{{#winning_linescores}}
  {{#stat_fouled_out}}
    {{lname}} fouled out!
  {{/stat_fouled_out}}
{{/winning_linescores}})
```
This code will first loop through all of the winning teams players, then check if the stat_fouled_out value exists, then will output the encapsulated text.

#### Generator Options
  - **field** ```string``` The field (abbreviation) to be evaluated.
  - **minValue** ```float``` A minimum threshold.  Values must meet or exceed this to pass the test
  - **maxValue** ```float``` A maximum threshold. Values must be equal or lower to this to pass
  - **preciseValue** ```float``` An exact threshold.  Rarely used, but allows you to target an exact value
  - **newField** ```string``` The name of the new, generated field.  In a linescores loop this will be available prepended with ```stat_```
  - **value** ```mixed``` The value to be assigned to ```newField```.  In true/false boolean checks, can be set to ```1``` or ```true```

#### Group Variables - Games

The **games** variable holds an array of **items**

#### Game Item Variables
  - **title** ```string``` Game title (if available)
  - **teams** ```array``` All participating teams (see below, team items)
  - **home** ```array``` The home team (if applicable)
  - **away** ```array``` The away team (if applicable)
  - **print_title** ```string``` If a print title exists, its value will be output with this variable
  - **custom** ```array``` Array of custom values

#### Team Item Variables
  - **record** ```array``` Wins, losses and ties
  - **conference_record** ```array``` Wins, losses and ties within conference
  - **score** ```int``` Final tally
  - **periods** ```array``` Score by period
  - **players** ```array``` Teamm's players (see below, player items)