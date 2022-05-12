---
date: 2022-01-22
aliases: []
---

```js
new Vue({
  el: "ID", // 在這個元素內的子元素使用Vue
  data: {
    // 變數，用物件寫法
    x: "string",
  },
  methods: {
    // 大部分函式在此放入
    cry(){
      alert();
    },
  },
  computed:{
    // 不傳入參數，但會回傳值的函式
    BNI(){
      return weight/(height**2);
    },
  },
})
```