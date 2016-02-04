# Widgets
> Pointslocal widgets provide a wrapper around the Pointslocal API for quickly building HTML widgets utilizing a simple template language.  In many cases Pointslocal will build these widgets for launch, but modifying or creating your own is incredibly easy.

#### Requirements
##### jQuery
> jQuery is not strictly required but is recommended. By default, jQuery is used in no-conflict mode.

##### Gameplan Javascript
> Place the call to the Gameplan Javascript after calling jQuery:
```html
  <script type="text/javascript" src="//cdn.pointslocal.com/gameplan.js"></script>
```
> or without jQuery:
```html
  <script type="text/javascript" src="//cdn.pointslocal.com/gameplan-nojq.js"></script>
```

#### Templating language
> Gameplan widgets allow injection of HTML templates that utilize a very basic templating language with some minor logic rules.  Since the API calls return JSON objects, you can use the templating language of your choice.

##### Variables
> Variables are expressed simply as {{name}}.  So if the widget returns a variable named **school_name**, it will be rendered anywhere {{school_name}} is in the template.
```html
<h1>{{school_name}} news</h1>
```

##### Loops
> Values returned as arrays by the widget can be iterated through a **.each** notation.
```html
{{teams.each}}<b>{{team_name}}</b>{{/teams.each}}
```

##### Existance or nonexistance of value
> You can check if a value exists or not through the **.exists** notation.
```html
{{team_name.exists}}Oh good, {{team_name}} is a value{{/team_name.exists}}
```

> Likewise, you can check if there is no value
```html
{{team_name.!exists}}No team name available!{{/team_name.!exists}}
```

##### Comparisons
> Checking for equality is done through the **is** notation.
```html
{{team_wins.is(0)}}Team is winless{{/team_wins.is}}
```

> Alternately, inequality through **not**:
```html
{{team_name.not(0)}}Phew, team has won a game.{{/team_name.not}}
```

> Both of the above functions convert the value to a string before handling comparisons.

> Greater than and less than comparisons are designated by **gt** and **lt** functions:
```html
{{team_wins.gt(12)}}Wow, this is a good season for a football team{{/team_wins.gt}}
```
```html
{{team_wins.lt(3)}}This team, however, has little chance of making the playoffs{{/team_wins.lt}}
```

### Using other templating languages
#### Mustache
https://github.com/janl/mustache.js/

#### Jade
https://github.com/pugjs/jade

#### Hogan
http://twitter.github.io/hogan.js/

#### Handlebars
http://handlebarsjs.com/