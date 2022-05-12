```js
for (起始值; 終止判斷; 計數) {
  執行敘述
}
for (let i = 1; i < 10; i++) {
  執行敘述
}
```
也可同時做兩個變數的計數，如:
```js
for (let i = 1, j = 1; i < 10; i++, j++) {
  執行敘述
}
```

for in 迴圈
```js
for (索引變數 in 物件變數){
  執行敘述
}
如
for (let key in object){
  console.log(key);
  consale.log(object[key]);
}
  //key是陣列物件的索引值，forin迴圈會只執行有值的陣列索引值，跳過undifine
  //for in也可用於陣列
```
break; 可跳出迴圈
continue; 跳過這次迴圈