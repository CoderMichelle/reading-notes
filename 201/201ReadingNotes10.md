# Debugging

+ Debugging is the process of finding errors. It involves a process of deduction.
+ If you understand execution contexts (which have two stages) and stacks, you are more likely to find the error process of deduction.
+ The console helps narrow down the area in which the error is located, so you can try to find the exact error.
+ JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.

1. Error
Generic error - the other errors are all based upon thes error
2. SyntaxError
Syntax has not been followed
MISMATCHING OR UNCLOSED QUOTES (SyntaxError: Unexpect ed EOF)
MISSING CLOSING BRACKET (SyntaxErr or : Expected token ')')
MISSING COMMA IN ARRAY
3. ReferenceError
Tried to reference a variable that is not declared/whithin scope
VARIABLE DOES NOT EXIST
VARIABLE IS UNDECLARED (ReferenceError: Can't find variable: height)
NAMED FUNCTION IS UNDEFINED(ReferenceError: Can't find variable: randomFunction)
4. TypeError
An unexpected data type that cannot be read
VALUE IS UNEXPECTED DATA TYPE (TypeError: 'undefined' is not a function (evaluating 'Document.write('Oops! ')'))
INCORRECT CASE FOR write() METHOD (TypeError: 'undefined' is not a function (evaluating 'document.Write('Oops!')'))
METHOD DOES NOT EXIST (TypeError: 'undefined ' is not a function (evaluating 'box.getArea()'))
DOM NODE DOES NOT EXIST (TypeError: 'null' is not an object (evaluating 'el .innerHTML = 'Mango''))
5. RangeError
Numbers not in acceptable range
NUMBER OUTSIDE OF RANGE (RangeError: Array size is not a small enough positive integer)
NUMBER OF DIGITS AFTER DECIMAL IN tofhed() CAN ONLY BE 0-20 (RangeError: toFixed() argument must be between 0 and 20)
6. URIError
encodeURI ().decodeURI(),and similar methods used incorrectly
7. EvalError
eval() function used incorrectly
8. NaNError
If you perform a mathematica l operation using a value that is not a number, you end up with the value of NaN, not a type error.

+ If you know that you may get an error, you can handle it gracefully using the try, catch, finally statements. Use them to give your users helpful feedback.