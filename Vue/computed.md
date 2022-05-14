---
date: 2022-05-14
aliases: []
---
# computed
可以監測變數是否改變並回傳新的值，如監測變數英吋(inch)的值回傳公分(cm):
```js
Vue.createApp({
  data(){
    return {
      inch: 1,
    }
  },
  computed:{
    cm(){
      return this.inch * 2.54
    },
  },
}).mount('#app');
```


computed亦可如函式般傳入參數以改變其他變數值，如除了監測變數英吋(inch)的值回傳公分(cm)，使用者輸入公分時亦改變英吋值
```js
Vue.createApp({
  data(){
    return {
      inch: 1,
    }
  },
  computed:{
    cm:{
      get(){
        return this.inch * 2.54;
      },
      set(val){
        this.inch = val / 2.54;
      },
    },
  },
}).mount('#app');
```
> 只有在有設定set時才可主動改變computed變數，否則會報錯
> 通常computed是被動改變數值

