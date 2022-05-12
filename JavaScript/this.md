---
date: 2022-01-22
aliases: []
---

```js
function test(){
  alert(this); // this -> object Window
}
```
此this代表函式執行當下的外層物件，this在函式執行時才存在

```js
let man = {
  name: "peter",
  sex: "male",
  sayHello(){
    alert(this); // this -> object Object
  }
}
```
同上，外層物件是Object

```js
()=>{
  alert(this);
}
```
箭頭函式裡面外面代表同一物件

Vue的this代表new Vue