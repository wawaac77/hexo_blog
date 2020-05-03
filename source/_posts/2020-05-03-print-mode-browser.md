---
title: Chrome设置print模式
date: 2020-05-03 20:04:23
tags: React
---

### 有时候我们想看网页打印出来是什么样子，难道只能`command + p`, 然后 preview print 吗？

**Chrome 设置一下，就可以在浏览器上直接看到打印的样子哦**

Command + Shift + J ==> 打开 developer console window

Command + Shift + P ==> 出现一个搜索

输入 render

选择 Drawer Show Rendering

然后在下面 Emulate CSS media type 下面那个 dropdown 里选择 print

**看到的东西就是打印出来会看见的样子啦**

### 想控制打印出来的样子，和浏览器显示的样子不一样，可以办到吗？

**可以的！只需要在 print mode 下 render 不同的 DOM 结构就可以啦~**

```tsx
export const StyledContainer = styled.div`
  #page-print {
    display: none;
  }
  @media print {
    #page-print {
      display: block;
    }
    #page-screen {
      display: none;
    }
  }
`;

const page = () => {
  return (
    <StyledContainer>
      <div id="page-screen">I'm looking at the browser.</div>
      <div id="page-print">I'm printing.</div>
    </StyledContainer>
  );
};
```
