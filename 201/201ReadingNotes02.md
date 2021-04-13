## Duckett HTML book: Chapter 2: Text
heading and paragraphs
bold, italic, emphasis ```<bold><italic><em><strong>```
structural and semantic markup h1,p,... vs em,strong,blockquote, q(within paragraph""), abbr,cite,defn,s(strikethrout)
html elements are used to describe the structure of the page (h1,p)
+ `<header>`
+ `<nav>`
+ `<main>`
+ `<content>`
+ `<article>`
+ `<aside>`
+ `<footer>`
These are some of the most commonly used ones. These new elements provide clearer code. Note `<div>`s are still very important for setting `<div.container>` classes (Emmet abbrev here).

There are also semantic tags that provide semantic info (em, defn)

+ White space is being collapsed
+ br linebreak forced and hr line through comments in html by using `ctr` ? produces `<!--a line of comment in html using Emmet-->`

+ Block elements start on a new line

+ Inline elemnts are displayed on the same text/display line - examples:

  div, ul, ol, li vs a-tag, span, strong, em, img tags

+ Iframes havent used these yet - interesting for map display - display another website in a window

+ Meta tags tell us about the page - they live inside the head tags - not visible on the page (unless ctrl U in chrome) - commonly used with name and content attributes
example `<meta name="description" content="Reading Notes on code102-session04-html" />`
name=keywords, name=robots

`&#60, &#62` special characters used to display reserved characters for code alled escape characters


Introducing CSS: 
+ what CSS does and how CSS works:
rules, properties, values
+ CSS treats each HTML element as if it appears inside its own box and uses rules 2 indicate how that element should look;
+ Rules are made up of selectors: element, class, ID; and declarations - what these elements should look like);

Declarations are made up of 2 parts:
+ properties of the element you want to change/style;
+ values of these properties; ie: color: pink;

3 ways to set css:
1. in header link href="style.css" rel="stylesheet"
2. in html header between style tags
3. inline with each element (not recommended!!!)

Block elements take up all the space they can per line, cause a page break - h1,p,div.vs. inline elements which 'snuggle up' - a,b,i,img,em,span.

+ universal selector *;
+ type selector h1, h3,...;
+ class selector .note;
+ id selectore #floating-top;
+ child selector li>a direct a from li;
+ descendant selector li a (not just direct);
+ h1+p - the first p after any h1;
+ ```:nth-child(5)```
+ ```:1st-child```
+ ```:last-child```

Cascading style sheet - rule cascades down to
+ child elements that are nested;
+ elements further down can be re -styled (last rule wins)
+ the more specific rule wins (specificity)
+ ```!important``` forces the issue;


+ font-family and color are inherited
+ most others are not but can be made to w propererty value inherit - ie: padding: inherit - from parent element.

Basic JavaScript Instructions

+ Scripts are a series of statements; like a recipe;
+ Scripts are very precise instructions eg a value has to be specified before it can be remembered;

// or /*mmmm*/ for comments;

 Expressions and Operators
 An expression results in a single value - 2 types
+ expressions that assign a value to a variable
+ expressions that use 2 or > values to return a single value

 Expressions rely on operators to calculate a value;
+ Assignment operators color = 'white'
+ Arithmetic operators area = 40 + 1
+ String operators 'Hi' + 'Lady Annabelle'
+ Comparison operators buy = 3 > 5 {false}
+ Logical operators buy = (5 > 3) && (2 < 4) {true}


+ Variables are used to temporarily store data stored in the script
+ Arrays are special types of variables that store more than 1 piece of info
+ JS distinguishes between - numbers(0-9) , strings(text - must b written on 1 line - + Open and closing quotes must be the same, Boolean (t/f)
+ Assignment operator - take right side and put it in bucket - variable;

```var (variable key word) price;```
```price = 3;```
OR write ```var price = 3;```
```var quantity = 14;```
```var total = quantity * price;```
```var el = document.getElementById('cost');```
```el.textContent = '$' + total;```
like a css tag the docwrite grabs the id="cost" element;
the el.textContent - writes this into it (and it could even include sth like a ```<h1>``` tag);

Naming convention for variables:
+ must begin with letter, $ or _ NOT a number
+ must contain letter, numbers, $ or _ mmmmm NOT - NOT .
+ NOT keywords or reserved words eg var
+ caseSensitive
+ use a name that describes whats stored firstName lastName (camelCase)
+ array stores a list of variables (>1);


Decisions and Loops only up to the section on switch statements

looking at a flowchart the browser will run different code in different situations;
conditional statements allow your code to make decisions about what 2do next;
comparison operators are used to compare to operands ```(===, !==, ==, !==, <,>,<=,=>)```;
logical operators ```(&&, ||, !)``` allow us 2 combine > than 1 set of comparisons;
if....else statements allow us 2 run 1 set of code if a condition is true and another if its false;

interesting:
+ var msg = '';
+ function congratulate(){
+ msg += 'Congrats';}
+ if (score>50) { congratulate();
+ msg += 'Proceed 2 next step';}
+ var el = document.getElementById('answer');
+ el.innerHTML = msg;
