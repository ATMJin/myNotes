---
date: 2024-05-10
aliases: 
tags:
  - RxJS
---
# map

用於對 Observable 中的每個值進行映射轉換。這個操作符類似於 JavaScript 中的 `Array.map()` 方法，它允許你對 Observable 中的每個值進行轉換，並返回一個新的 Observable，其中包含映射後的值。

## 範例

```typescript
const source = from([1, 2, 3, 4, 5]);

source.pipe(
  map(value => value * 2)
).subscribe(result => console.log(result));
// 2
// 4
// 6
// 8
// 10
```