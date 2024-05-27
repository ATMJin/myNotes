---
date: 2024-05-10
aliases: 
tags:
  - RxJS
---
# merge

將多個 [[Observable]] 合併成一個 Observable。當任何一個源 Observable 發出新值時，`merge` 操作符就會將這個值合併到最終的合併 Observable 中。

## 範例

```typescript
// 第一個 Observable 每秒發出一個值，並只取前 5 個值
const observable1 = interval(1000).pipe(take(5));
// 第二個 Observable 每兩秒發出一個值，並只取前 3 個值
const observable2 = interval(2000).pipe(take(3));

const mergedObservable = merge(observable1, observable2);

const startSeconds = new Date().getSeconds();
mergedObservable.subscribe((value) => {
    console.log("秒數:", new Date().getSeconds() - startSeconds, "值:", value);
});
```

結果: 

秒數: 1 值: 0
秒數: 2 值: 0
秒數: 2 值: 1
秒數: 3 值: 2
秒數: 4 值: 1
秒數: 4 值: 3
秒數: 5 值: 4
秒數: 6 值: 2

彈珠圖: 

```
observable1: -0-1-2-3-4|
observable2: ---0---1---2|
      merge: -0-01-2-13-4-2|
```

也就是說當每秒發送一次跟每兩秒發送一次的Observable，
merge後新的Observable會同時有每秒發送一次跟每兩秒發送一次的特性。