---
title: Functions
layout: post
---

## How to create functions in JavaScript

There are three basic ways to create a function in JavaScript (we'll also go into nuances). I write this yet another post on JS functions not to bore the world wide web, but purely for my own enjoyment and education. I am 99.21% sure no one reads these posts. This is for my future self, so he won't hate me for not writing shit down when I understand them and can articulate them in his own words.

Functions are blocks of code that can be called to do... you know, whatever you wrote them to do, repeatedly. The basic structure is a definition (so you know what to call/execute later) and a function body (the code that does whatever you want it to do). Related to the first two, there're also parameters you input into the function, and if you want to, you can have the function return something... anything.

So here goes:

### Way Number 1

Function Expression and Variable Assignment
```javascript
const myFunction = function(param1,param2) {
    //do something 
    //return something
}
```
Function expressions are pretty neat, because they imply that while a function reference can be assigned to a variable just like a primative value or object, it doesn't have to be assigned. We'll get to that later. For now, just know that this is one way of creating a function.

### Way Number 2

Function Declaration 
```javascript
function myFunction(param){
    //do something
    //return something
}
```

Function declarations omit the assignment to a variable 
### Way Number 3

Arrow functions - ES6 forward
```javascript
const myFunction = (param) => {
    //do something
    //return something
}
```