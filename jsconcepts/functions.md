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

The biggest difference is in the way the JavaScript interpreter (in ours and most cases, the browser and NodeJS) parses the code. Specifically, *when* the function is available for invocation. On parsing a piece of code, the browser goes from top to bottom; along the way, it takes note of variable definitions and assignments (including function expressions), for which it creates a placeholder in memory for, as well as what gets assigned to it. But that's it, just parses the code and takes note, unless it encounters a function declaration: 

*Function declarations get treated differently. When the browser parses and encounters a function declartion, they are hoisted, meaning they are immediately available for use when the browser goes through and executes the code, in whatever order they are placed.*

Hoisting is the reason functions can be declared *after* they have been invoked in lexical order (the way its written). The first pass of your code by the browser hoisted the function declaration so it is available on execution.

### Way Number 3

Arrow functions - Available in ES6
```javascript
const myFunction = (param) => {
    //do something
    //return something
}
```

Introduced in ES6, arrow functions are the most fun out of the three methods of creating functions. It has the exact same shape as a function expression, different only in its shorthand elegance. Writing arrow functions always gives me the feeling I'm some cool hacker, writing code no one understands. Kind of the same feeling you get writing ternery operators or Regex, or using logical operators as default conditions. 

Without getting too mired in the details, arrow functions differ in one other major way to both function expressions and declarations. It's in its relationship to the 'this' object. Using non-arrow functions, your 'this' references detach from the intended object if 'this' is invoked within a callback that is once removed from direct ownership of the function. Arrow functions, however, will seek out the closest object in direct parent lineage to attach 'this' to. Please go here for a more detailed treatment and code samples.

That's it for functions. Now get coding!