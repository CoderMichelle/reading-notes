
# HTML Chapter 1, 8, 17 from Duckett HTML book:
- HTML describes the structure of pages
- HTML code is made up of characters that live inside angled brackets--these are called HTML *elements*
- Elements are usually made up of two **tags**, and opening tag and a closing tag
- Each element tells the browser something about the info that sits between its opening and closing tags
- HTML uses elements describe the structure of the pages
- Tags act like containers, they tell you something about the info inside them.
- <p> - < =left-angle bracket, p = character, and > = right-angle bracket.
- Attributes tell us more about the element; they have a name and a value.
- Extra Markup + starts with !DOCTYPE html tells the sbrowser you are using the latest version - ref basic structure - html (head, body(header(nav),main(section, article, aside),footer)); + comments
+ Id (only 1 per page) and class (multiple times per page) attributes for element tags;
+ Block elements take up all the space (per line) they can and cause a line break after;
+ Inline elements snuggle up to before and after;
+ Div tags group text and elements in a block;
+ Span tags group text and elements inline;
+ Frames create a window in a window (think google maps);
+ Meta tags add meta data - not displayed (think search optimization, keywords, robots; description that shows up in tab ontop);
+ Escape characters (think `&copy; &lt; &gt;` )

#### HTML Layout
using new element tags vs just generic div - basic structure
html (head, body(header(nav),main(section (article(hgroup)),(article(hgroup)),aside(section)),footer));

#### HTML Process & Design
+ It's important to understand who your target audience is and why they would come to your website; what info they want to find; and when and why they would return;(update roadmap/plan for the site/for pages/sections)
+ Site maps allow u 2 plan the structure of the site; remember the visitor and her/his perspective is key, not the site owner; card sorting technique;
+ Wireframes - a simple sketch of the key info that needs 2go on each page;
+ Design is about communication;
+ Visual hierarchy helps visitors 2 understand what u r trying 2 tell them;
+ You can differentiate between pieces of info using (think text) size, color and style BOLD;
+ You can use grouping and similarity 2 help simplify the info u present; whitespace between unrelated items

#### JS Chapter 1: “The ABC of Programming” 
#### What is a script? How do I create one? for a webpage?
+ A script is like a recipe,a handbook or a manual -it's a series of instructions that a computer follows to achieve a goal.
+ Each time the script runs it might only use a subset of all the instructions
+ Computers approach tasks in a different way than humans, so your instructions must let the computer solve the tasks programmatically;
1. Define the goal;
1. Design the script;
1. Code each step;
Flowchart on page 18 and another one on page 23;
Learn to think how computers think - solving problems programmatically;

#### How do computers fit in with the world around them?
- computers create models of the world using data;
- objects can have their own:
+ properties (name and value);
+ events (triggered by user input or webpage itself);
+ methods (like a function - what interpreter does with objects);

webbrowsers create models of what they display - of the web pages that are shown and of the window it is shown in;
the document object represents an html page;
using the document object, you can access and change what content users see on the page and respond to how they interact with it; that document object has properties, methods, events;
also creates a new object for each element on the page;
see the DOM document object model;

browser receives html code - creates a model of the page and stores it - it has a hierarchy (document - html - head - title+link,....) - elements, text, attributes... - it uses a rendering engine to show that page on the screen(CSS);

#### How do I write a script for a webpage
layered - html - css - javascript; progressive enhancements;
```<script src="js/add-content.js"></scriptEND>;```
does NOT show in source code - but the link to js file does
```<script>document.write('<h3>Welcome!</h3>')</script>;```


