---
date: 2022-01-22
update: 2022-03-16
aliases: [falsy]
---
# falsy value
在需要做布林值轉換時(如在if判斷式內)，會將下列值轉換成false
- `false`
- 空字串，如`''`、`""`、` `` `
- `0`，包括`+0`、`-0`、`0n`
- `null`
- `undefined`
- `NaN`
反之非以上falsy value的值即為[[truthy value]]

要注意的是如果單純與false做比較，只有0、空字串、false會\==false