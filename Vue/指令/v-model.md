---
date: 2022-01-22
aliases: []
---
# v-model

雙向綁定變數。
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

```


## 修飾符