---
date: 2022-03-05
aliases: [Promise]
---
# Promise
Promise 是一個表示非同步運算的最終完成或失敗的物件。

## 方法
### then(function)
程式執行正常時執行，可無限連結如`promise.then().then().then()......`
`return`會回傳新的Promise物件

### catch(function)
程式執行錯誤時執行