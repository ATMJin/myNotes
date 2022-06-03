---
date: 2022-06-03
aliases: []
---
# never
never 代表不可能存在的值，而 never 值可以指派給任何型別，但只能接收 never。
可用來做型別防衛
```ts
let value: number | string;
switch (typeof value) {
  case "number":
    break;
  case "string":
    break;
  default:
    let fin: never = value;
}
// 因為一開始就宣告value只能是number或string
// 所以進入defult的狀況只能是never
// 若是never以外的型別就會報錯
```

