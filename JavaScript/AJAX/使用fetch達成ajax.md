---
date: 2022-03-05
aliases: []
---
## 一般GET方法
### 1. 最初用[[fatch]]取得路徑回傳值
```js
fetch(url,[options])
  .then((response) => {
      //成功結果處理
  })
  .catch((error) => {
      //錯誤結果處理
})
```

### 2. 再將回傳值轉成可處理之格式
```js
fetch(url)
  .then(function(res){
  return res.json()
});
```
亦可寫成[[箭頭函式]]
```js
fetch(url)
  .then(res => res.json());
```

其中可轉換的格式有:
-  `response.json()`：把資料轉成JSON格式
-  `response.text()`：把資料轉成text格式(變成純字串)
-  `response.blob()`：把資料轉成Blob物件
-  `response.formData()`：把資料轉成FormData物件
-  `response.arrayBuffer()`：把資料轉成二進制數組

### 3. 再對格式化後的資料進行操作
```js
fetch(url)
  .then(res1 => res1.json())
  .then(res2 => {
    console.log(res2)
});
```


## POST
