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

## 改變陣列內容後畫面不會重新渲染
> 此為 Vue 2 會出現的問題
> Vue 3 將原本的更新機制從 Object.defineProperty 改成 ES6 的 Proxy API 後已將問題改善。

例如以下案例:
```html
<button @click="changeArr">Enter</button>

<p v-for="item in arr">{{ item }}</p>
```
```js
new Vue({
  data: {
    arr:["a", "b", "c"],
  },
  methods: {
    changeArr(){
      this.arr[2] = "d";
      alert(this.arr[2]);
    },
  },
}).$mount('#app');
```

按下 button 時從 alert 確認陣列 arr 已被改變，但畫面沒有依最新內容重新渲染。
因為 Vue 2 是使用 Object.defineProperty 的 set 與 get 去改變與讀取變數值，在某些情況下雖然值被改變了但 set 沒被觸發，所以畫面不會重新渲染。
因此 Vue 為以下常用的陣列方法重新改寫，使其也會觸發。
- push( )
- pop( )
- shift( )
- unshift( )
- splice( )
- sort( )
- reverse( )

除此之外也可用以下方法強制更新
```js
methods: {
  changeArr(){
    this.$set(this.arr, 2, "d")
    alert(this.arr[2]);
  },
}
```