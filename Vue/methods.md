---
date: 2022-05-14
aliases: []
---
# methods
可放入任意函式，如:
```js
Vue.createApp({
  data(){
    return {
      price: 200,
      count: 5,
    }
  },
  methods:{
    alert(){
      if (this.count < 0){
        window.alert("error!");
      }
    },
    totel(){
      this.alert();
      return this.price * this.count;
    },
  },
}).mount('#app');
```