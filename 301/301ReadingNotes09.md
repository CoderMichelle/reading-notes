# Functional Programming Concepts
# Refactoring Javascript for Readability

resoures https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa
## Concepts of Functional Programming in Javascript

Functional programming concepts like immutability and pure function are big advantages to build side-effect-free functions, so it is easier to maintain systems
# What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia
Pure functions

The first fundamental concept we learn when we want to understand functional programming is pure functions. But what does that really mean? What makes a function pure?

So how do we know if a function is pure or not? Here is a very strict definition of purity: It returns the same result if given the same arguments (it is also referred as deterministic) It does not cause any observable side effects
It returns the same result if given the same arguments

It returns the same result if given the same arguments Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:

Why is this an impure function? Simply because it uses a global object that was not passed as a parameter to the function. Now imagine some mathematicians argue that the PI value is actually 42and change the value of the global object. Our impure function will now result in 10 * 10 * 42 = 4200. For the same parameter (radius = 10), we have a different result. Let's fix it!

TA-DA 🎉! Now we’ll always pass thePI value as a parameter to the function. So now we are just accessing parameters passed to the function. No external object. For the parameters radius = 10 & PI = 3.14, we will always have the same the result: 314.0 For the parameters radius = 10 & PI = 42, we will always have the same the result: 4200
It does not cause any observable side effects

Examples of observable side effects include modifying a global object or a parameter passed by reference. Now we want to implement a function to receive an integer value and return the value increased by 1.

We have the counter value. Our impure function receives that value and re-assigns the counter with the value increased by 1. Observation: mutability is discouraged in functional programming. We are modifying the global object. But how would we make it pure? Just return the value increased by 1. Simple as that.

See that our pure function increaseCounter returns 2, but the counter value is still the same. The function returns the incremented value without altering the value of the variable.

If we follow these two simple rules, it gets easier to understand our programs. Now every function is isolated and unable to impact other parts of our system.

Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. We don’t need to think of situations when the same parameter has different results — because it will never happen.
Immutability

Unchanging over time or unable to be changed.

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value. In Javascript we commonly use the for loop. This next for statement has some mutable variables.

For each iteration, we are changing the i and the sumOfValue state. But how do we handle mutability in iteration? Recursion!

So here we have the sum function that receives a vector of numerical values. The function calls itself until we get the list empty (our recursion base case). For each "iteration" we will add the value to the total accumulator. With recursion, we keep our variables immutable. The list and the accumulator variables are not changed. It keeps the same value.
## Refactoring JavaScript for Performance and Readability (with Examples!)

There's a middle ground between speed and comprehension and that's where good code lives.

see article for examples of code refactoring.

It's important to get your code right the first time because in many businesses there isn't much value in refactoring. Or at least, it's hard to convince stakeholders that eventually uncared for codebases will grind productivity to a halt.
