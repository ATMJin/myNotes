一般在編輯HTML時，最前面會進行以下宣告，告知瀏覽器
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>

<body>
</body>
</html>
```

---
## \<!DOCTYPE html>
宣告文件是以HTML5的形式撰寫，單一`html`即表示為HTML5，大幅簡化輸入

如在HTML4為
```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
           "http://www.w3.org/TR/html4/strict.dtd">
```
XHTML為
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
          "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

---
## \<html lang="en">
宣告頁面的語系，以增加搜尋引擎最佳化(search engine optimization，SEO)。

---
## \<[[meta]] charset="UTF-8">
指定字元編碼為UTF-8

---
## \<meta http-equiv="X-UA-Compatible" content="IE=edge">
專門針對IE8的設定
- content="edge" 以最高級別的可用模式顯示內容
- content="IE=Edge,chrome=1" 如果IE有安裝Google Chrome Frame，那麼就走安裝的元件

---
## \<meta name="viewport" content="width=device-width, initial-scale=1.0">
設定viewport(視口)
- width=device-width 指定瀏覽器頁面的寬度同裝置 (device) 的寬度
- initial-scale=1.0 指定畫面初始縮放比例為 100%，即不放大也不縮小
- user-scalable=no 禁止使用者用手指縮放比例