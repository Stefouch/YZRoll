## YZRoll
A Year Zero Roll object.

**Kind**: global class

* [YZRoll](#YZRoll)
    * [new YZRoll(game, author, name)](#new_YZRoll_new)
    * _instance_
        * [.author](#YZRoll+author) : <code>string</code>
        * [.name](#YZRoll+name) : <code>StringResolvable</code>
        * [.game](#YZRoll+game) : <code>string</code>
        * [.pushCount](#YZRoll+pushCount) : <code>number</code>
        * [.maxPush](#YZRoll+maxPush)
        * [.isFullAuto](#YZRoll+isFullAuto) : <code>boolean</code>
        * [.dice](#YZRoll+dice) : [<code>Array.&lt;YZDie&gt;</code>](#YZDie)
        * [.size](#YZRoll+size) : <code>number</code>
        * [.pushed](#YZRoll+pushed) : <code>boolean</code>
        * [.successCount](#YZRoll+successCount) : <code>number</code>
        * [.baneCount](#YZRoll+baneCount) : <code>number</code>
        * [.attributeTrauma](#YZRoll+attributeTrauma) : <code>number</code>
        * [.gearDamage](#YZRoll+gearDamage) : <code>number</code>
        * [.stress](#YZRoll+stress) : <code>number</code>
        * [.panic](#YZRoll+panic) : <code>number</code>
        * [.rof](#YZRoll+rof) : <code>number</code>
        * [.mishap](#YZRoll+mishap) : <code>boolean</code>
        * [.hasNegative](#YZRoll+hasNegative) : <code>boolean</code>
        * [.pushable](#YZRoll+pushable) : <code>boolean</code>
        * [.setFullAuto([bool])](#YZRoll+setFullAuto) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.setGame(game)](#YZRoll+setGame) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.setName(name)](#YZRoll+setName) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.push()](#YZRoll+push) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.addBaseDice(qty)](#YZRoll+addBaseDice) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.addSkillDice(qty)](#YZRoll+addSkillDice) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.addGearDice(qty)](#YZRoll+addGearDice) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.addNegDice(qty)](#YZRoll+addNegDice) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.addStressDice(qty)](#YZRoll+addStressDice) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.addDice(type, qty, [range], value, [operator])](#YZRoll+addDice) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.removeDice(type, qty)](#YZRoll+removeDice) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.getDice(type)](#YZRoll+getDice) ⇒ [<code>Array.&lt;YZDie&gt;</code>](#YZDie)
        * [.pool()](#YZRoll+pool) ⇒ <code>Object</code>
        * [.sum(type)](#YZRoll+sum) ⇒ <code>number</code>
        * [.baseSix(type)](#YZRoll+baseSix) ⇒ <code>number</code>
        * [.count(type, seed)](#YZRoll+count) ⇒ <code>number</code>
        * [.modify(mod)](#YZRoll+modify) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.toPhrase()](#YZRoll+toPhrase) ⇒ <code>string</code>
        * [.toString()](#YZRoll+toString) ⇒ <code>string</code>
        * [.toValues()](#YZRoll+toValues) ⇒ <code>string</code>
        * [.valueOf()](#YZRoll+valueOf) ⇒ <code>number</code>
    * _static_
        * [.DIE_TYPES](#YZRoll.DIE_TYPES) : <code>Array.&lt;string&gt;</code>
        * [.ROLLREGEX](#YZRoll.ROLLREGEX) : <code>RegExp</code>
        * [.parse(rollString, game, author, name)](#YZRoll.parse) ⇒ [<code>YZRoll</code>](#YZRoll)
        * [.substitute(str)](#YZRoll.substitute) ⇒ <code>string</code>

<a name="new_YZRoll_new"></a>

### new YZRoll(game, author, name)

| Param | Type | Description |
| --- | --- | --- |
| game | <code>string</code> | The game of the roll |
| author | <code>string</code> | The author of the roll |
| name | <code>string</code> | The name of the roll |

<a name="YZRoll+author"></a>

### YZRoll.author : <code>string</code>
The author of the roll.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+name"></a>

### YZRoll.name : <code>StringResolvable</code>
The name of the roll.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+game"></a>

### YZRoll.game : <code>string</code>
The game used.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+pushCount"></a>

### YZRoll.pushCount : <code>number</code>
The number of times the roll was pushed.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+maxPush"></a>

### YZRoll.maxPush
The maximum number of times the roll can be pushed.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+isFullAuto"></a>

### YZRoll.isFullAuto : <code>boolean</code>
Tells if the roll can be pushed at will.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+dice"></a>

### YZRoll.dice : [<code>Array.&lt;YZDie&gt;</code>](#YZDie)
The dice pool of the roll.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+size"></a>

### YZRoll.size : <code>number</code>
The total number of dice in the roll.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+pushed"></a>

### YZRoll.pushed : <code>boolean</code>
Whether the roll was pushed or not.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+successCount"></a>

### YZRoll.successCount : <code>number</code>
The quantity of successes.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+baneCount"></a>

### YZRoll.baneCount : <code>number</code>
The quantity of ones (banes).

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+attributeTrauma"></a>

### YZRoll.attributeTrauma : <code>number</code>
The quantity of traumas ("1" on base dice).

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+gearDamage"></a>

### YZRoll.gearDamage : <code>number</code>
The quantity of gear damage ("1" on gear dice).

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+stress"></a>

### YZRoll.stress : <code>number</code>
The quantity of stress dice.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+panic"></a>

### YZRoll.panic : <code>number</code>
The quantity of panic ("1" on stress dice).

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+rof"></a>

### YZRoll.rof : <code>number</code>
The Rate of Fire (number of Ammo dice - *Twilight 2000*).

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+mishap"></a>

### YZRoll.mishap : <code>boolean</code>
Tells if the roll is a mishap (double 1's).

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+hasNegative"></a>

### YZRoll.hasNegative : <code>boolean</code>
Tells if there are negative dice.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+pushable"></a>

### YZRoll.pushable : <code>boolean</code>
Tells if the roll is pushable.

**Kind**: instance property of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll+setFullAuto"></a>

### YZRoll.setFullAuto([bool]) ⇒ [<code>YZRoll</code>](#YZRoll)
`maxPush = 10` to avoid abuses.de.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll, with unlimited pushes

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [bool] | <code>boolean</code> | <code>true</code> | Full Auto yes or no |

<a name="YZRoll+setGame"></a>

### YZRoll.setGame(game) ⇒ [<code>YZRoll</code>](#YZRoll)
Sets the game played.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll, with a new game parameter

| Param | Type | Description |
| --- | --- | --- |
| game | <code>string</code> | The game |

<a name="YZRoll+setName"></a>

### YZRoll.setName(name) ⇒ [<code>YZRoll</code>](#YZRoll)
Sets the name of the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll, renamed

| Param | Type | Description |
| --- | --- | --- |
| name | <code>string</code> | The new name of the roll |

<a name="YZRoll+push"></a>

### YZRoll.push() ⇒ [<code>YZRoll</code>](#YZRoll)
Pushes the roll, following the YZ rules.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll, pushed
<a name="YZRoll+addBaseDice"></a>

### YZRoll.addBaseDice(qty) ⇒ [<code>YZRoll</code>](#YZRoll)
Adds a number of base dice to the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll

| Param | Type | Description |
| --- | --- | --- |
| qty | <code>number</code> | The quantity to add |

<a name="YZRoll+addSkillDice"></a>

### YZRoll.addSkillDice(qty) ⇒ [<code>YZRoll</code>](#YZRoll)
Adds a number of skill dice to the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll

| Param | Type | Description |
| --- | --- | --- |
| qty | <code>number</code> | The quantity to add |

<a name="YZRoll+addGearDice"></a>

### YZRoll.addGearDice(qty) ⇒ [<code>YZRoll</code>](#YZRoll)
Adds a number of gear dice to the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll

| Param | Type | Description |
| --- | --- | --- |
| qty | <code>number</code> | The quantity to add |

<a name="YZRoll+addNegDice"></a>

### YZRoll.addNegDice(qty) ⇒ [<code>YZRoll</code>](#YZRoll)
Adds a number of negative dice to the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll

| Param | Type | Description |
| --- | --- | --- |
| qty | <code>number</code> | The quantity to add |

<a name="YZRoll+addStressDice"></a>

### YZRoll.addStressDice(qty) ⇒ [<code>YZRoll</code>](#YZRoll)
Adds a number of stress dice to the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll

| Param | Type | Description |
| --- | --- | --- |
| qty | <code>number</code> | The quantity to add |

<a name="YZRoll+addDice"></a>

### YZRoll.addDice(type, qty, [range], value, [operator]) ⇒ [<code>YZRoll</code>](#YZRoll)
Adds a number of dice to the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| type | <code>string</code> |  | The type of dice to add ("base", "skill", "gear" or "neg") |
| qty | <code>number</code> |  | The quantity to add |
| [range] | <code>number</code> | <code>6</code> | The number of faces of the die |
| value | <code>number</code> | <code></code> | The predefined value for the die |
| [operator] | <code>string</code> | <code>&quot;&#x27;+&#x27;&quot;</code> | The operator of the die |

<a name="YZRoll+removeDice"></a>

### YZRoll.removeDice(type, qty) ⇒ [<code>YZRoll</code>](#YZRoll)
Removes a number of dice from the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll

| Param | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | The type of dice to remove |
| qty | <code>number</code> | The quantity to remove |

<a name="YZRoll+getDice"></a>

### YZRoll.getDice(type) ⇒ [<code>Array.&lt;YZDie&gt;</code>](#YZDie)
Gets all the dice of a certain type.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)

| Param | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | Dice type to search |

<a name="YZRoll+pool"></a>

### YZRoll.pool() ⇒ <code>Object</code>
Reduces the Roll to a dice pool.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+sum"></a>

### YZRoll.sum(type) ⇒ <code>number</code>
Gets the sum of the dice of a certain type.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: <code>number</code> - The summed result

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| type | <code>string</code> | <code>null</code> | "base", "skill", "gear", "neg", etc... |

<a name="YZRoll+baseSix"></a>

### YZRoll.baseSix(type) ⇒ <code>number</code>
Gets the base-six sticky-result of the dice of a certain type.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: <code>number</code> - The sticked result

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| type | <code>string</code> | <code>null</code> | "base", "skill", "gear", "neg", etc... |

<a name="YZRoll+count"></a>

### YZRoll.count(type, seed) ⇒ <code>number</code>
If `seed` is omitted, counts all the dice of a certain type.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: <code>number</code> - Total count

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| type | <code>string</code> |  | The type of the die |
| seed | <code>number</code> | <code></code> | The number to search. |

<a name="YZRoll+modify"></a>

### YZRoll.modify(mod) ⇒ [<code>YZRoll</code>](#YZRoll)
Applies a difficulty modifier to the Year Zero Roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - This roll, modified

| Param | Type | Description |
| --- | --- | --- |
| mod | <code>number</code> | Difficulty modifier (bonus or malus) |

<a name="YZRoll+toPhrase"></a>

### YZRoll.toPhrase() ⇒ <code>string</code>
Turns the YZRoll into a roll phrase.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+toString"></a>

### YZRoll.toString() ⇒ <code>string</code>
Returns the description of the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
**Returns**: <code>string</code> - The roll described in one sentence
<a name="YZRoll+toValues"></a>

### YZRoll.toValues() ⇒ <code>string</code>
Returns only the values of the dice in the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll+valueOf"></a>

### YZRoll.valueOf() ⇒ <code>number</code>
Returns the primitive value of the roll.

**Kind**: instance method of [<code>YZRoll</code>](#YZRoll)
<a name="YZRoll.DIE_TYPES"></a>

### YZRoll.DIE\_TYPES : <code>Array.&lt;string&gt;</code>
Allowed die types.

**Kind**: static constant of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll.ROLLREGEX"></a>

### YZRoll.ROLLREGEX : <code>RegExp</code>
Regex used to parse rolls.

**Kind**: static constant of [<code>YZRoll</code>](#YZRoll)
**Read only**: true
<a name="YZRoll.parse"></a>

### YZRoll.parse(rollString, game, author, name) ⇒ [<code>YZRoll</code>](#YZRoll)
Parses a roll resolvable string into a Year Zero Roll object.

**Kind**: static method of [<code>YZRoll</code>](#YZRoll)
**Returns**: [<code>YZRoll</code>](#YZRoll) - Parsed roll

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| rollString | <code>string</code> |  | A roll resolvable string |
| game | <code>string</code> |  | The game of the roll |
| author | <code>string</code> |  | The author of the roll |
| name | <code>string</code> | <code>null</code> | The name of the roll |

<a name="YZRoll.substitute"></a>

### YZRoll.substitute(str) ⇒ <code>string</code>
Parses and sums all roll resolvable strings in a text.

**Kind**: static method of [<code>YZRoll</code>](#YZRoll)
**Returns**: <code>string</code> - Processed replacements

| Param | Type | Description |
| --- | --- | --- |
| str | <code>string</code> | Text to parse |

<a name="YZDie"></a>

## YZDie
Year Zero Die with type. The die is rolled if no value is predefined.

**Kind**: global class

* [YZDie](#YZDie)
    * [new YZDie(range, type, [value], [operator])](#new_YZDie_new)
    * [.range](#YZDie+range) : <code>number</code>
    * [.type](#YZDie+type) : <code>string</code>
    * [.result](#YZDie+result) : <code>number</code>
    * [.previousResults](#YZDie+previousResults) : <code>Array.&lt;number&gt;</code>
    * [.operator](#YZDie+operator)
    * [.pushCount](#YZDie+pushCount) : <code>number</code>
    * [.pushed](#YZDie+pushed) : <code>boolean</code>
    * [.pushable](#YZDie+pushable) : <code>boolean</code>
    * [.roll()](#YZDie+roll) ⇒ <code>number</code>
    * [.push()](#YZDie+push) ⇒ <code>number</code>
    * [.modifyRange(mod)](#YZDie+modifyRange) ⇒ <code>number</code>

<a name="new_YZDie_new"></a>

### new YZDie(range, type, [value], [operator])

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| range | <code>number</code> |  | The number of faces of the die |
| type | <code>string</code> |  | The type of the die |
| [value] | <code>number</code> | <code>0</code> | Any predefined value for the die |
| [operator] | <code>string</code> | <code>&quot;&#x27;+&#x27;&quot;</code> | The operator of the die |

<a name="YZDie+range"></a>

### YZDie.range : <code>number</code>
The number of faces of the die.

**Kind**: instance property of [<code>YZDie</code>](#YZDie)
<a name="YZDie+type"></a>

### YZDie.type : <code>string</code>
- `modifier`: Cannot be rolledot pushable+ not pushable

**Kind**: instance property of [<code>YZDie</code>](#YZDie)
<a name="YZDie+result"></a>

### YZDie.result : <code>number</code>
The result of the die.

**Kind**: instance property of [<code>YZDie</code>](#YZDie)
<a name="YZDie+previousResults"></a>

### YZDie.previousResults : <code>Array.&lt;number&gt;</code>
All previous results, in order of appearance.

**Kind**: instance property of [<code>YZDie</code>](#YZDie)
<a name="YZDie+operator"></a>

### YZDie.operator
- `/`: divisioncationie.

**Kind**: instance property of [<code>YZDie</code>](#YZDie)
<a name="YZDie+pushCount"></a>

### YZDie.pushCount : <code>number</code>
Number of times this die has been pushed.

**Kind**: instance property of [<code>YZDie</code>](#YZDie)
**Read only**: true
<a name="YZDie+pushed"></a>

### YZDie.pushed : <code>boolean</code>
Whether this die has been pushed.

**Kind**: instance property of [<code>YZDie</code>](#YZDie)
**Read only**: true
<a name="YZDie+pushable"></a>

### YZDie.pushable : <code>boolean</code>
Whether the die can be pushed (according to its type).

**Kind**: instance property of [<code>YZDie</code>](#YZDie)
**Read only**: true
<a name="YZDie+roll"></a>

### YZDie.roll() ⇒ <code>number</code>
Rolls the die.

**Kind**: instance method of [<code>YZDie</code>](#YZDie)
**Returns**: <code>number</code> - The new result
<a name="YZDie+push"></a>

### YZDie.push() ⇒ <code>number</code>
Pushes the die, according to its type.

**Kind**: instance method of [<code>YZDie</code>](#YZDie)
**Returns**: <code>number</code> - The result, Whether it has been pushed or not.
<a name="YZDie+modifyRange"></a>

### YZDie.modifyRange(mod) ⇒ <code>number</code>
Modifies the range of the die by a number of steps.

**Kind**: instance method of [<code>YZDie</code>](#YZDie)
**Returns**: <code>number</code> - Number of increased steps

| Param | Type | Description |
| --- | --- | --- |
| mod | <code>number</code> | Positive or negative number of steps |