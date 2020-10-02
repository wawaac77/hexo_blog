---
title: Smart ways of doing console.log
date: 2020-10-02 18:23:07
tags:
---

Here is an example. If we want to log these variables:

```js
const apple = { color: "red", number: 10 };
const peach = { color: "pink", number: 12 };
const blueberry = { color: "blue", number: 50 };
```
### Utilize object

```js
console.log({ apple, peach, blueberry });
```

By putting variables in object, it can easily log varabile name and values all together.

### Utilize array

```js
console.log([ apple, peach, blueberry ]);
```

By putting variables in array, it can log a table in browser dev tools if they have many common fileds.
