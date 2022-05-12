---
date: 2022-03-05
aliases: []
---

fetch是`window`物件的方法，會回傳一個[[Promise物件]]。
語法為
```js
let promise = fetch(url, [options])
```
亦可直接寫
```js
fetch(url, [options])
```

如果只有url路徑沒有options，則預設請求方法為GET。

## [[使用fetch達成ajax]]