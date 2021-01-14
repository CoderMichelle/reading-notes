## HTML Links, JS Functions, and Intro to CSS Layout

### HTML Links:
+ ```Links are created using the <a> element.```  
  ```<a href="http:....."><a/>```
+ If you are linking to a page within your own site, it is best to use relative links rather than qualified URLs. 
+ You can create links to open email programs with an email address in the "to" field.
+ You can use the id attribute to target elements within a page that can be linked to.

### Layout:
+ <div> elements are often used as containing elements to group together sections of a page.
+ Browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning.
+ The float property moves content to the left or right of the page and can be used to create multi-column layouts. (Floated items require a defined width.)
+ Pages can be fixed width or liquid (stretchy) layouts.
+ Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels (to demonstrate its relevance without scrolling).
+ Grids help create professional and flexible designs.
+ CSS Frameworks provide rules for common tasks.
+ You can include multiple CSS files in one page.

### JS Functions, Methods, and Objects:
+ Programmers use functions, methods, and objects to organize their code.
+ Functions consist of a series of statements that have been grouped together because they perform  specific task.
+ A method is the same as a function, except methods are created inside (and are part of) and object.
+ Programmers use objects to create models of the world using data, and objects are made up of properties and methods. 
+ A browser comes with a set of objects that act like a toolkit for creating interactive web pages. 
+ Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements).
+ Grouping together the statements that are required to answer a question or perform a task helps organize your code.
+ To create a function, you give it a name and then write the statements needed to achieve its task inside the curly braces; this is known as a **function** **declaration**.
+ function sayHello() {
    document.write('Hello!');
  }
+ Having declared the function, you can then execute all of the statements between its curly braces with just one line of code. This is known as **calling** **the** **function**.
+ Sometimes a function needs specific information to perform its task. In such cased, when you declare the function you give it parameters. Inside he function, the parameters act like variables.
+ When you call a function that has parameters, you specify the values it should use in the parentheses that follow its name. The values are called arugments, and they can be provided as values or as variables.
+ Some functions return information to the code that called them. For example, when they perform a calculation, they return the result. 
+ Functions can return more than one value using an array. For example, a function can calculate the area and volume of a box.
+ The location where you declare a varible will affect where it can be used within your code. If you declare it within a function, it can only be used within that function. This is known as the variable's **scope**.
+ Global variables use more memory. The browser has to remember them for as long as the web page using them is loaded.Local variables are only remembered during the period of time that a function is being executed.