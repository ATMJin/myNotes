---
date: 2022-05-13
aliases: []
---
# 建立Vue實體並掛載
Vue需要建立實體並掛載到頁面上後才能執行並顯示。
Vue2跟Vue3的掛載方式不同
在建立實體時不一定要先宣告一個vm變數，也可以直接`.mount`掛載

## Vue 2
Vue 2 的掛載方式有兩種:
```js
const vm = new Vue({
});

vm.$mount('#app');
```
或
```js
const vm = new Vue({
  el: "#app", 
})
```

## Vue 3
```js
const vm = Vue.createApp({
});

vm.mount('#app');
```


## 掛載節點

`vm.mount()`(或`vm.$mount()`)可在建立Vue實體後再建立節點再掛載。

```js
const vm = new Vue({});

const el = document.createElement('div');
document.body.appendChild(el);

vm.$mount(el);
```

其中el可使用DOM物件或CSS[[選擇器]]，CSS選擇器並不限於ID，但只會掛載到第一個。

