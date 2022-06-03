---
date: 2022-06-03
aliases: []
---
# any

在宣告時使用 any 型別可以讓變數像原本在JS內一樣在不同型別中任意轉換。
但這樣會失去使用TS的目的。
可改用 [[unknown]] 型別避免過度彈性。

可在設定檔中設定禁止 any 的型態推論
`tsconfig.json`
```json
{
  "compilerOptions": {
    "noImplicitAny": true
  }
}
```

