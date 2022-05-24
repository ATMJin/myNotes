---
date: 2022-05-23
aliases: []
---
# 取得DOM元素
為了取得頁面上DOM元素，可在元素標籤上加上`ref`屬性，並給與屬性值，最後在 Vue 中藉由此屬性取得此DOM元素。
在 Options API 與 Composition API 下做法略有不同。

## Options API
Options API 直接使用`this.$refs.屬性值`來取得元素
```html
<div ref="test">AAA</div>
```
```js
console.log(this.$refs.test.innerText) // AAA
```

## Composition API
Composition API 需宣告 `ref(null)` 進行綁定
```js
import {ref} from 'vue';

setup(){
  const test = ref(null);
  console.log(test.value.innerText) // AAA
}
```


## v-for
當要抓取由 v-for 建立出的 DOM 時，有以下兩種方法:

### 設定相同 ref
```html
<div 
  v-for ="i in 5 " 
  ref="test"
>
  {{i}}
</div>
```

用此方法抓到的`this.$refs.test`或是`test.value`會是一個陣列，用陣列操作即可

### 綁定 ref 陣列
>Composition API 的用法
```html
<div 
  v-for ="i in 5 " 
  :ref="el => { test[i] = el }"
>
  {{i}}
</div>
```
如此`test.value`也會是一個陣列