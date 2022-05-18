---
date: 2022-01-22
aliases: []
---
# v-for
可產生許多相同元素
`v-for="item in items"`
items是Vue中陣列或物件的變數名稱
item是從陣列或物件取得的值在此加了v-for的元素的變數名稱，可任意取名。

亦可加入索引值 index
`v-for="(item, index) in items" :key="index"`
在物件的情況下，索引值順序在不同瀏覽器可能會有差異。

物件也可輸出 key
`v-for="(item, key, index) in items" :key="index"`

> 因為 Vue 會重複利用元素，因此加入 key 屬性可避免不可預期的錯誤。


## 數字
若將items改成自然數，可渲染出指定數量的元素，索引由1開始。

## 排序與過濾
v-for 排序與過濾的功能，只能額外用 [[computed]] 或 [[methods]] 產生新的陣列後再使用 v-for