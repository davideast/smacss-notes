# State and Themes

|--------+-----------+
|        |   MODULE  |
| STATE  +-----------+
|        +-----------+
|        |   LAYOUT  |
|+-------+-----------+
+--------------------+
|        BASE        |
+--------------------+

**State** is about changing the look and feel of something that may be a module or a layout.

You typically don't apply a state to a base element. They're applied to specific modules.

### States

Like a module variation (sub-module) but indicate a JavaScript dependency.

+---------------------+
|        THEME        |
+---------------------+
|---------+-----------+
|         |   MODULE  |
|  STATE  +-----------+
|         +-----------+
|         |   LAYOUT  |
|+--------+-----------+
+---------------------+
|        BASE         |
+---------------------+

### Themes

Theming is the ability to swap in and out color themes in realtime.

- Only for on-the-fly style changes
- Usually aren't needed
- Preprocessors can help
* UI Kits

Chose 6 colors:
- base-color
- lighter
- lightest
- darker
- darkest
- selected-state

### Categorization
- Every style we write serves on of these purposes whether we're aware of it or not.
- Isolating code allows for easier reuse, testing, and debugging. 
- Categorizing reveals patterns; easier to identify when things break the pattern.