---
date: 2022-05-16
aliases: [元組]
---
# Tuple
推測是來自中國的翻譯，參考自數組。
可限定陣列內型別的順序。
```ts
let 變數:[型別1, 型別2, 型別3, ...]
```
使用如:
```ts
let arr:[number, string, boolean];

arr = [123, "abc", true];
```
或是
```ts
enum gender {male, female};
type myname = string;
type age =number;
type mail = string;

type Person = [myname, gender, age, mail];

let data:Person[] = [];
data.push(['Mark', gender.male, 18, 'abc@gmail.com']);
```