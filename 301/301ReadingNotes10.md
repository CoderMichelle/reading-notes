# Readings: THE CALL STACK

resources The Call Stack defined on MDN https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors

Understanding the JavaScript Call Stack https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c

JavaScript error messages https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/

Additional Resources JavaScript errors reference on MDN https://developer.mozilla.org/en-US/docs/Glossary/Call_stack
## The Call Stack and Debugging JavaScript error messages && debugging

What is call stack?

A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function. Any functions that are called by that function are added to the call stack further up, and run where their calls are reached. When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing. If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error. Summary:

we start with an empty Call Stack. Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.
JavaScript error messages && debugging

Types of error messages:

Reference errors when we try to use a variable that is not yet declared you get this type os errors. when we assign variable value before declaration.
Syntax errors

occurs when we have something that cannot be parsed in terms of syntax

Range errors

Type errors occurs when the types (number, string and so on we are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

Debugging

To debug JS code, the easiest and maybe the most common way its to simply console.log() the variables we want to check or, by using chrome developer tools.

Using Node.js with Visual Studio Code we can press the debug tab and add a configuration similar to this:

"version": "0.2.0", "configurations":[ { "type": "node", "request": "launch", "name": "Launch Program", "program": "${workspaceRoot}/index.js" } ] // debugger by pressing F5 Another way to find errors in code, using call stack in the console, which is the path that program has taken to reach the point were we set a breaking point or were we have an error.

For call stack it’s better to navigate when you have names to your functions

Handling errors Good practice to handle errors is try to catch the errors so we can fallback to a default state of our application in case of an error.

(function testing(){ function add(a, b) { try { var result = a + b return result.split('') } catch (error) { console.error('add went wrong ->', error) return [] // default value } } var stringResult = add("1", "2") var numberResult = add(1, 2) })() Tools to avoid runtime errors:

quokka tool to evaluate your code as you type
to make sure style guide is consistency

## JavaScript Error Handling & Debugging (JS Book page 449-486)

Order of execution

2 find the source of an error it helps to know how scripts are processed.
Execution Contexts

There is one global execution context; plus each function creates a new execution context. they respond to variable scope;

global context - global variable scope

function context - function level scope
The stack

The JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks (or piles) the new function on top of the current task.
Execution Context and Hoisting

Each time a script enters a new execution context, there are two phases:

prepare (the new scope is created; variables, functions and arguments are created);
execute (now it can assign values 2 variables, reference functions and run their code, execute statements);

Undertstanding Scope

In the interpreter each execution context has its own variables object. It holds the variables, functions and parameters available within it. Each execution context can also acess its parents variables object.

functions are linked to the object they were defined within. So for each execution context, the scope is the current execution contexts variables object plus the variables object for each parent execution context. Imagine each function is a nesting doll. The chilkdren can ask their parents for information in their variables. But the parents cannot get variables from their children. Each child will get the same answer from the same parent.

If a JavaScript statement generates an error, then it throws an exception . At that point, the interpreter stops and looks for exception-handling code.
ERROR OBJECTS

Error objects can help you find where your mistakes are and browsers have tools to help you read them.

There are seven types of built-in error objects in JavaScript.

Error

Generic error - the other errors are all based upon this error

SyntaxError

Syntax has not been followed
MISMATCHING OR UNCLOSED QUOTES (SyntaxError: Unexpect ed EOF)
MISSING CLOSING BRACKET (SyntaxErr or : Expected token ')')
MISSING COMMA IN ARRAY

ReferenceError
Tried to reference a variable that is not declared/whithin scope
    
VARIABLE DOES NOT EXIST
VARIABLE IS UNDECLARED (ReferenceError: Can't find variable: height)
NAMED FUNCTION IS UNDEFINED(ReferenceError: Can't find variable: randomFunction)

TypeError

An unexpected data type that cannot be read
VALUE IS UNEXPECTED DATA TYPE (TypeError: 'undefined' is not a function (evaluating 'Document.write('Oops! ')'))
INCORRECT CASE FOR write() METHOD (TypeError: 'undefined' is not a function (evaluating 'document.Write('Oops!')'))
METHOD DOES NOT EXIST (TypeError: 'undefined ' is not a function (evaluating 'box.getArea()'))
DOM NODE DOES NOT EXIST (TypeError: 'null' is not an object (evaluating 'el .innerHTML = 'Mango''))

RangeError

Numbers not in acceptable range
NUMBER OUTSIDE OF RANGE (RangeError: Array size is not a small enough positive integer)
NUMBER OF DIGITS AFTER DECIMAL IN tofixed() CAN ONLY BE 0-20 (RangeError: toFixed() argument must be between 0 and 20)

URI Error

encodeURI ().decodeURI(),and similar methods used incorrectly ? & # : ;

Eval Error

eval() function used incorrectly

NaN

If you perform a mathematica l operation using a value that is not a number, you end up with the value of NaN, not a type error.

Debugging Workflow

WHERE IS THE PROBLEM?

First, you should try to narrow down the area where the problem seems to be. In a long script, this is especially important. Look at the error message, it tells you:

The relevant script that caused the problem.
The line number where it became a problem for the interpreter. (As you will see, the cause of the error may be earlier in a script; but this is the point at which the script could not continue.)
The type of error (although the underlying cause of the error may be different).

WHAT EXACTLY IS THE PROBLEM?

Once you think that you might know the rough area in which your problem is located, you can then try to find the actual line of code that is causing the error.

when you have set breakpoints u can c if the variables around them have the values you would expect them to have. If not look earlier in the script.
Break down parts of the code to test smaller pieces of the functionality.

Write values of variables into the console.
Call functions from the console to check if they are returning what you would expect them to.
Check if objects exist and have the methods/properties that you think they do.

Check the numbers of parameters for a function or number of items in an array.

## Debugging Tips

ANOTHER BROWSER

Some problems are browser- specific. Try the code in another browser to see which ones are causing a problem.

ADD NUMBERS

Write numbers to the console so you can see which the items get logged. It shows how far your code runs before errors stop it.
STRIP IT BACK
Remove parts of code, and strip it down to the minimum you need. You can do this either by removing the code altogether, or by just commenting it out.
EXPLAINING THE CODE
SEARCH - Stack Overflow is a Q+A site for programmers.

## COMMON ERRORS

GO BACK TO BASICS

JavaScript is case sensitive so check capitalization.
If you did not use var to declare the variable, it will be a global variable, and its value could be overwritten elsewhere (either in your script or by another script that is included in the page).
If you cannot access a variable's value, check if it is out of scope (declared within a function that you are not within).
Do not use reserved words or dashes in variable names.
Check that your single I double quotes match properly.
Check that you have escaped quotes in variable values.
Check in the HTML that values of your id attributes are unique.

MISSED/ EXTRA CHARACTERS

Check that there are no missing closing braces } or parentheses )
Check that there are no commas inside a , } or ,) by accident.
Always use parentheses to surround a condition that you are testing.
Check the script is not missing a parameter when calling a function.
undefined is not the same as nu11 : nu11 is for objects, undefi ned is for properties, methods, or variables.
Check that your script has loaded (especially CDN files).
Look for conflicts between different script files.

DATA TYPE ISSUES

Using= rather than == will assign a value to a variable, not check that the values match.
If you are checking whether values match, try to use strict comparison to check datatypes atthesame time. (Use === rather than ==.)
Inside a switch statement. the values are not loosely typed (so their type will not be coerced).
Once there is a match in a switch statement, all expressions will be executed until the next br eak or return statement is executed. If you are using the parseInt() method, you might need to pass a radix (the number of unique digits including zero used to represent the number).
