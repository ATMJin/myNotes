---
date: 2022-05-14
aliases: []
---
# filters
> ==此屬性已在Vue 3被移除。==

可將值傳入處理後回傳，實際可用[[methods]]代替

```js
new Vue({
  filters:{
    capitalize(value){
      if (!value) {
        return '';
      }
      value = value.toString();
      return value.charAt(0).toUpperCase() + value.slice(1);
    },
  },
}).$mount('#app');
```

使用方法為在HTML模板中用`|`分隔值與欲使用的濾鏡
```html
<p>{{ msg }}</p>
<p>{{ msg | capitalize }}</p>
<p>{{ msg | capitalize | smalllize }}</p>
```