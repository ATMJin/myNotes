---
date: 2022-01-22
aliases: []
---
# v-model

雙向綁定變數，為[[v-bind]]與[[v-on]]的結合。
改變原始變數的值會改變網頁中的值，改變網頁中的值也會改變原始變數的值。
只能用在`<input>`,`<select>`, `<textarea>` 或components
但`<input type="file">`不能使用

## radio / checkbox

radio:
```html
<input type="radio" name="sex" id="male" value="male" v-model="vsex">
<label for="male">male</label>

<input type="radio" name="sex" id="female" value="female" v-model="vsex">
<label for="female">female</label>

<span>{{ sex }}</span>
```
```js
Vue.createApp({
  data(){
    return {
      vsex: "male",
    }
  }
}).mount("#app");
```

checkbox的變數用陣列控制:
```html
<input type="checkbox" name="skill" id="html" value="html" v-model="skill">
<input type="checkbox" name="skill" id="css" value="css" v-model="skill">
<input type="checkbox" name="skill" id="JavaScript" value="JavaScript" v-model="skill">
<input type="checkbox" name="skill" id="PHP" value="PHP" v-model="skill">

<span>{{ skill }}</span>
```
```js
Vue.createApp({
  data(){
    return {
      skill: [],
    }
  }
}).mount("#app");
```
>若只有單一checkbox，也可以使用布林值來控制。

## select
```html
<select name="" id="" v-model="alphabet">
  <option value="" disabled>請選擇</option>
  <option value="a">a</option>
  <option value="b">b</option>
  <option value="c">c</option>
  <option value="d">d</option>
</select>

<span>{{ alphabet || "未選擇" }}</span>
```
```js
Vue.createApp({
  data(){
    return {
      alphabet: "",
    }
  }
}).mount("#app");
```
>第一個選項使用disabled是避免使用者送出預設值。


## 修飾符

### .lazy
原本v-model是監聽input事件，只要輸入即馬上反應。
`.lazy`則改成change事件，聚焦離開輸入框時才會反應。

### .number
會嘗試將值轉型成數字，避免字串型別的數字直接被處理。

### .trim
過濾前後空白字元。