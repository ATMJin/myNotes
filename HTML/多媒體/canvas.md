---
date: 
aliases: 
tags:
  - HTML
---

一個能產生影像的區域，必須先設定範圍，並使用JS繪圖

本質上是一張png，但可由JS再添加內容。
若要更改大小，要使用HTML標籤屬性，不能用CSS。用CSS雖然外觀會改變，但本質大小不變。

一開始要宣告平面或立體
```js
let canvas = document.getElementById("canvas");
let context = canvas.getContext("2d");
```
然後再繪圖

## 矩形
```js
context.rect(x0, y0, x1, y1); //設定形狀
context.fill(); //填滿
context.stroke(); //畫邊框
context.clear(); //清除

//直接填滿形狀或畫框
context.fillRect(x0, y0, x1, y1);
context.strokeRect(x0, y0, x1, y1);
context.clearRect(x0, y0, x1, y1);

//設定填滿內容或邊框
context.fillStyle="red";
context.strokeStyle="blue";
context.lineWidth=10;  //邊框寬度是同時向內向外增加

```

## 線條
```js
context.moveTo(x, y); //設定起始點
context.lineTo(x, y); //畫到(x,y)
context..stroke();

context.closePath(); //設定頭尾封閉
context.beginPath(); //開始路徑，重設路徑
```

## 文字
```js
context.fillText("words", x, y); //實心文字
context.strokeText("words", x, y); //空心文字

context.font="字型樣式"
context.textBaseline="對齊線" 
//文字預設定位在baseline，即(x,y)在首字左下baseline，文字在定位的右上
```

## 陰影
```js
context.shadowColor="";
context.shadowOffsetX=""; //方向
context.shadowOffsetY="";
context.shadowBlur=""; //擴散
```

## 曲線
```js
//弧線，使用徑度，右方為0，順轉false
context.arc(x, y, r, rad0, rad1, 順逆) 
//以(xc1, yc1)(xc2, yc2)、(xc1, yc1)(x0, y0)為切線的指定半徑圓的弧線，從(x0, y0)畫到接(xc1, yc1)(xc2, yc2)直線
context.moveTo(x0, y0)
context.arcTo(xc1, yc1, xc2, yc2, r)
//貝茲二次曲線
context.moveTo(x0, y0);
context.quadraticCurveTo(cpx, cpy, x1, y1);
//貝茲三次曲線
context.moveTo(x0, y0);
context.bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x1, y1);
```

## 其他
```js
context.translate(x, y)  //變更原點座標
```
