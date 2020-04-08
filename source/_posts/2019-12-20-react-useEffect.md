---
title: React - useEffect究竟代表lifecycle的哪部分？
date: 2020-04-07 10:39:46
tags: React
---

### useEffect应用情景
1. 当我们使用useQuery从后端取到data之后，有时我们想把data存到redux里面，那么就可以在useEffect里面，将data作为dependency，当data有变化时执行一个react的action，dispatch这个data到redux里面。e.g.
```ts
    useEffect(() => {
        if (data) {
            storeDataToRedux(data); //an action to dispatch to redux store
        }
    }, [data, storeDataToRedux]);
```
2. 当一个backend query依赖于其他地方传给它的parameter时，也可以把param作为useEffect的dependency，并在useEffect里面执行那个backend query。e.g.
```ts
    useEffect(() => {
        const getCustomerDetail = async () => {
            const { data } = await apolloClient.query({
                query: GET_CUSTOMER_DETAIL
                variables: { customerNumber }
            });
            store.dispatch(storeCustomerDetail(data.getCustomerDetail));
        };
        getCustomerDetail();
    }, [apolloClient, store, getCustomerDetail]);
```
### 有趣的问题
如果我们在useEffect里面添加一个console.log()的话，我们就可以清楚的知道useEffect在什么时候执行了。我们会发现当来到使用useEffect的当前页面，和离开当前页面的时候，都会执行。我们可能会奇怪，为什么离开页面了，useEffect还会执行一次呢？

### 原因来自official document
> If you’re familiar with React class lifecycle methods, you can think of useEffect Hook as componentDidMount, componentDidUpdate, and componentWillUnmount combined.

所以，下一次观察到，来到这个页面useEffect就执行力2次，离开这个页面又执行1次，就不会再奇怪啦。
