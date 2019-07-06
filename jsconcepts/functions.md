---
title: Functions
layout: post
---
## What are functions?

Functions are blocks of code you can call to perform a specific task. The basic structure is a function name (so you know what to call/execute later) and a function body where you insert code for what you want it to do. Functions can also require parameters to be inputted as arguments when they are called (invoke, executed). Not only can you create functions to do stuff, you can also create it to do stuff *and* return a result. In JavaScript, functions are considered first class citizens, meaning they are treated just like variables. They can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable. 

## How do I create functions in JavaScript

There are three basic ways to create a function in JavaScript. I write this yet another post on JS functions not to bore the world wide web, but purely for my own enjoyment and education. I am 99.21% sure no one reads these posts. This is for my future self, so he won't hate me for not writing shit down when I understand them and can articulate them in his own words.


So here goes:

### Way Number 1

Function Expression and Variable Assignment
```javascript
const myFunction = function(param1,param2) {
    //do something 
    //return something
}
```
Function expressions are pretty neat, because they imply that while a function can be created and assigned to a variable just like a primative value or object, it doesn't have to be assigned. When functions don't get assigned to a variable, they are known as anonymous functions. We'll get into this topic more later, but for now, just know that this is one way of creating a function.

### Way Number 2

Function Declaration 
```javascript
function myFunction(param){
    //do something
    //return something
}
```

Function declarations omit the assignment to variable of "Way Number 1", and instead declare a name for the function as well as its parameters/definition (what it does) in a single syntax block. 

Both methods of creating functions are valid, and acceptable in JavaScript. Both give you the same result for the same input and neither is easier to write than the other. So what the heck is the difference?

The biggest difference is in the way the JavaScript interpreter (in ours and most cases, the browser and NodeJS) treats/executes the function. Specifically, *when* the function is available for invocation. On execution of a piece of code, the interpreter goes from top to bottom; along the way, it takes note of variable definitions and assignments (including function expressions), for which it creates a placeholder in memory for, as well as what gets assigned to it. But that's it, 

*Function declarations, on the other hand, get treated differently. They are hoisted, meaning they are immediately available for use by executing code in whatever order they are placed.*

Hoisting is the reason functions can be declared *after* they have been invoked in lexical order. The first pass of your code by the interpreter hoisted the function declaration so it is available on execution.

### Way Number 3

Arrow functions - Available in ES6
```javascript
const myFunction = (param) => {
    //do something
    //return something
}
```

Introduced in ES6, arrow functions are the most fun out of the three methods of creating functions. It has the exact same shape as a function expression, different only in its shorthand elegance. Writing arrow functions always gives me the feeling I'm some cool hacker, writing code no one understands. Kind of the same feeling you get writing ternery operators or Regex, or using logical operators as default conditions. 

Without getting too mired in the details, arrow functions differ in one major way to both function expressions and declarations. It's in its relationship to the 'this' object. Wow, say that five times. Whereas non-arrow functions are bound to the object within which they were created (sometimes it's the window object), arrow functions seek out the closest parent object and bind to it. Because of this behavior, functions passed as variables (callbacks) will behave differently depending on how they were created (arrow or non-arrow).   