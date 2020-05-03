---
title: Export & Import in React
date: 2020-04-11 07:12:08
tags: react
---

We can often see: 
`export * from './Components';`

### What does * mean?

> A module can wrap one or more modules and combine all their exports using `export * from './Components';` syntax

一般这句code放在Components同一个folder的index.ts里面。

##### 这样引用的好处是：path就写到index这一层就可以了，当Component地址变化时，比如又给Component包裹一层folder，那只需要修改`index.ts`里面的import就好，project里面所有其他地方的import都不需要改动。

当然也可以选择不用index.ts

那么直接在Component想export的小部件里前面，加`export` 或 `default export` 就好.

React Apps可以看作是可交互的小部件的集合，就好像乐高一样，我们把它搭建成一个成品。

那么相同样子、用途的部件的重复使用是很重要的。我们常常把一些共用的部件放在另外的file里面，然后export出去，在需要的地方再import就可以啦。

### import默认的export
每一个module可以声明最多一个default export。我们想引用时，只需要import它的地址就可以了。import的声明给它一个我们想要的名字。像这样 `import AnyNameYouLike from '../../Components'`

### import命名过的部件
每一个module可以export很多不同名字的部件。我们可以引用它的名字 `import { Header } from '../../Components`

还可以重名成我们需要的名字 `import { Header as PageHeader } from '../../Components`

### 还可以一起引用
 `import AnyNameYouLike， { Header } from '../../Components'`


------------------------
React Apps can be seen as a collection of interactive components.