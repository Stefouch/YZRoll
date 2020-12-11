# Year Zero Roll

A package for rolling Year Zero Engine dice for Free League Publishing roleplaying games.

## Installation & Usage

To install the latest version on npm:
```
npm install yearzero-roll
```

To import the Class, add the following line at the top of your JavaScript file:
```js
const YZRoll = require('yearzero-roll');
```

To create a new roll, use the following code:
```js
let roll = new YZRoll();
```

## Example

```js
// Creates the roll for the Twilight 2000 4E game.
let roll = new YZRoll('t2k');

// Adds one D10 base die and rolls it.
roll.addDice('base', 1, '10');

// Adds one D6 skill die and rolls it.
roll.addSkillDice('skill', 1);

// Pushes the roll.
roll.push();

// Gets the number of successes & banes.
let successes = roll.successCount;
let banes     = roll.baneCount;
```

## See Also

* [API documentation](https://github.com/Stefouch/yearzero-roll/blob/main/DOCUMENTATION.md)