---
title: jest spyOn怎么用呢？
date: 2020-05-07 20:51:03
tags: TDD, jest
---

有时候我们从第三方 library 里面 import 了，或者自己写了一个 object，里面有我们想用的 function A，是给另外一个 function B 使用。

我们想测试 B 真的用了 A 吗？怎么做呢？

`jest.spyOn`这个时候就可以很方面的帮到我们哦！

> jest.spyOn(object, methodName)

以下就是一个来自官方文档，超级直观的例子

例子：
```js
const video = {
  play() {
    return true;
  }
};

module.exports = video;
```

例子的测试
```js
const video = require("./video");

test("plays video", () => {
  const spy = jest.spyOn(video, "play");
  const isPlaying = video.play();

  expect(spy).toHaveBeenCalled();
  expect(isPlaying).toBe(true);

  spy.mockRestore();
});
```

#### 可能会被不小心忽略，出bug的地方
如果我们有好几次测试，都spyOn同一个function，如果每次开始测试前没有清除之前的测试的关联的话，可能会出错哦。

比如我们expect这个function在这个test里面`.toHaveBeenCalledTimes(1)`, 被执行一次。

如果之前测试也执行过一次，我们又没有重新设置mock的话，`toHaveBeenCalledTimes`就会是2次哦。

可以用 `jest.resetAllMocks()` 来轻松解决。

效果和在每一个test之前都加上`.mockReset()`是一样的。

> Resets the state of all mocks. Equivalent to calling .mockReset() on every mocked function. Returns the jest object for chaining.

#### 以下来自官方文档

Creates a mock function similar to jest.fn but also tracks calls to object[methodName]. Returns a Jest mock function.

Note: By default, jest.spyOn also calls the spied method. This is different behavior from most other test libraries. If you want to overwrite the original function, you can use jest.spyOn(object, methodName).mockImplementation(() => customImplementation) or object[methodName] = jest.fn(() => customImplementation);
