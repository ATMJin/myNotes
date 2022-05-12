---
date: 2022-01-07
aliases: []
---
```js
 let url = "tt.json";
 let request = new XMLHttpRequest();
 request.open('GET', url);
 request.responseType = 'json';
 request.send();  

 let tt;
 request.onload = function () {
 tt = request.response;
 }
```