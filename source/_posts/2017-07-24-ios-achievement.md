---
title: 2017-07-24 【iOS今天的收获】最简单的返回前一个viewController并局部更新的方法
date: 2017-07-24 12:26:59
tags: ios
---
## 应用情景
类似于微博，前一个tableViewController列表中的某个内容点赞后，点击内容进入detailViewController，在里面取消赞，再返回前一页的tableViewController的时候，局部更新刚刚的改变，而不是整个[table reloadData].

## 如何局部更新
第一个想解决的是，如何局部更新。我之前不确定，局部更新会不会令table的内容从头开始，答案是不会，table会保留点击进入下一个页面那一刻的位置。table指定位置更新的代码是：

```objective-c
NSIndexPath *indexPath=[NSIndexPath indexPathForRow:3 inSection:0];

[tableView reloadRowsAtIndexPaths:[NSArray arrayWithObjects:indexPath,nil] withRowAnimation:UITableViewRowAnimationNone];
```
## Possible solutions
那么更新代码放在哪里呢？是viewController1的viewWillAppear？还是viewController2的viewWillDisappear?

indexPath的信息从哪里来呢？是viewController1本身可以存贮？还是viewController2 利用delegate来passValue过去？

其实这些方案应该都可以得到正确的效果，只是复杂度不同。

## 最简单的方法
最后我发现最简单的方法是，在viewController1的viewWillAppear里面，

```objective-c
-(void)viewWillAppear:(BOOL)animated{

    [self.tableView reloadRowsAtIndexPaths:[NSArray arrayWithObjects:[self.tableView indexPathForSelectedRow],nil] withRowAnimation:UITableViewRowAnimationNone];
}
```

## 这个方法回答了以上两个疑问：

1. IndexPath 来自本身tableView的`indexPathForSelectedRow`，之所以我们可以取得这个数据，是因为返回此viewController1它位置停留在点击跳转的那一刻，意味着系统一定记录了这个位置，那么我们就可以取得这个数据为我们所用。

    其实我尝试过 `@property (strong, nonatomic) NSIndexPath *recordIndexPath;` 来记录选中的indexPath，但是返回时这个数据清空了，它不是全局变量，viewController是来controller view的，不记录这个变量的具体解释以后再仔细研究。


2. 返回前一页也会触发viewWillAppear，第一次加载也会触发viewWillAppear，这个意味着要小心第一次加载触发时想利用的数据还不存在而导致的错误。


