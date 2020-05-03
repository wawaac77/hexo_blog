---
title: Throw error
date: 2020-05-03 19:57:33
tags: javascript, typescript
---

`throw new Error("Here is error message.");`

在一个function里面，这句代码执行之后，这个function里面后面的代码都不会执行哦。

可以试试如果把它不放在`if`或者`try`那样的条件里面，直接写在function中间某个位置，这句代码下面的代码都是灰色的。