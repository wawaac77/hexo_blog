---
title: prototype是什么？ What's prototype?
date: 2020-05-03 15:48:21
tags: javascript
---

`Prototype` 没有什么神秘和复杂。它只是Javascript中你创建的每一个function都有的，指向object的一个属性，

不过arrow function没有，因为arrow function不是一个constructor function。

--------------
> `Prototype` is a property that every function you create in Javascript has that points to an object. 

Prototype is just an object that every function (except arrow function) has.

But arrow function does not have Prototype, because arrow function is not a constructor function.
