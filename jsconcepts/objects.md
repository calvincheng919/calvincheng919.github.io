---
title: Objects
layout: post
Date: 
---

## What is an object?

If you learn nothing else from this article, know this: An object is simply a model of something in the real world. 

A ball is an object. 

So let's model a ball digitally. It won't be perfect, but hopefully when we're done, it will "look" somewhat like a ball. 

In real life, objects such as balls, have properties. A ball has size, small, medium or large. A ball can have buoyancy, and weight. And lastly, there are actions that a ball is able to perform. A ball, for instance, can bounce and roll. At its core, a real life object can be abstracted into a list of attributes (properties) and actions (methods).

```
Object: ball
  size: medium
  buoyant: yes
  weight: 16oz 
  bounce: Do bouncy thing
  roll: Do rolly thing
```

Let's model that in JavaScript!

In Javascript, just like in real life, an object can be defined by a list of properties and methods. Take, for instance, the object ball described as a JavaScript object literal (just means a piece of code and represents an object):

```javascript
//For simplicity sake, our ball will not have any actions
//For simplicity sake, we are using 'var' to declare a variable 
var ball = {
  size: 'medium',
  buoyant: true,
  weight: '16oz'
}
```

## Why are objects important?
