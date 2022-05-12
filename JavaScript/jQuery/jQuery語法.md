---
date: 2022-01-10
aliases: []
---
基本語法
``` js
$(選擇器).動作()
```
事件執行的函示要使用匿名函式function(){}
如:
``` js
$(this).hide()
$("p").click(function(){})
$("h1").css("color","red")
```

可將許多動作串接在同一行
```js
$("div").click(function(){}).css("background","red")
```

一次設定許多[[CSS屬性]]時使用物件的寫法
```js
$("div").css({
  height: "100px",
  width: "200px",
  border: "1px solide black",
})
```