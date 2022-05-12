---
date: 2022-01-10
aliases: []
---
# 新增document物件
1. 建立標籤
```js
document.createElement("標籤名稱");
let image = document.createElement("img");
```
2. 設定屬性方法
```js
image.src="";
image.width=300;
image.style.width="300px";
image..addEventLisener();
```
3. 找到parentNode，加入
```js
parentNode.appendChild(image);
parentNode.insertBefore(image, brotherNode);
parentNode.replace(image, brotherNode);
//jQ
//$(父).append(子)
//$(子).appendTo(父)
```
4. 刪除
```js
parentNode.removeChild(image);
//jQ: $(父).remove(子)
```


