---
title: Functions
layout: post
---

## How to create functions in JavaScript

There are three basic ways to create a function in JavaScript. I write this yet another post on JS functions not to bore the world wide web, but purely for my own enjoyment and education. I am 99.21% sure no one reads these posts. This is for my future self, so he won't hate me for not writing shit down when I understand them and can articulate them in my own words.

Functions are blocks of code that can be called to do... you know, whatever you wrote them to do. The basic structure is a declaration (so you know what to call/execute later) and a function body (the code that does whatever you want it to do). Related to the first two, there's also parameters you input into the function, and if you want to, you can have the function return something... anything.

So here goes:

### Way Number 1

Variable declaration and assignment
```javascript
const myFunction = function(param1,param2) {
    //do something 
    //return something
}
```
### Way Number 2

```javascript
function myFunction(param){
    //do something
    //return something
}
```
### Way Number 3

```javascript
const myFunction = (param) => {
    //do something
    //return something
}
```