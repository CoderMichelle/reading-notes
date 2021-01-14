HTML Lists, CSS Boxes, JS Control Flow

HTML Lists:

There are three types:
+ ordered -- using numbers
+ Unordered -- using bullets
+ Definition lists -- used to define terminology

Lists can be nested inside one another.

CSS Boxes:

+ CSS treats each HTML element as if it has its own box.
+ You can use CSS to control the dimensions of a box.
+ You can also control the borders, margins and padding for each box with CSS.
+ It is possible to hide elements using the display and visibility properties.
+ Block-level boxes can be made into inline boxes, and inline boxes made into block-level boxes.
+ Legibility can be improved by controlling the width of boxes containing text and the leading.
+ CSS3 has introduced the ability to create image borders and rounded borders.

JS:

+ In arrays, index values start at 0, not 1.
+ Values in an array are accessed as if they are in a numbered list (starting at zero).
+
// Create the array
var colors = ['white', 'black','custom',];

// Update the third item in the array
colors[2] = 'beige';

//Get the element with an id of colors
var el = document.getElementById('colors');

//Replace with third item from the array
el.textContent = colors[2];

Decisions & Loops:

+ Conditional statements allow your code to make decisions about what to do next.
+ Comparison operators (===, !==, ==), !=, <, >,<=, =>) are used to compare two operands.
+ Logical operators allow you to combine more than one set of comparison operators.
+ if...else statements allow you to run one set of code if a condition is true, and another if it is false.
+ switch statements allow you to compare a value against possible outcomes (and also provides a default option if none match).