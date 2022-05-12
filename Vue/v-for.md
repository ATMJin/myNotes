---
date: 2022-01-22
aliases: []
---

可產生許多相同元素
`v-for="item in items"`
items是Vue中陣列或物件的變數名稱
item是從陣列或物件取得的值在此加了v-for的元素的變數名稱。

`v-for="(item, index) in items" :key="index"`