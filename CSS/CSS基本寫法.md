可在\<head>標籤內使用\<style>編寫CSS樣式，或用\<link>加入外部css檔，或在標籤內使用行內CSS

```html
<head>
  <style>
    選擇器 {
      屬性: 值 ;
	  屬性: 值 ;
    }
  </style>
</head>

<body>
	<p style="屬性: 值;"></p>
</body>
```

外部css檔亦可使用`@import "another.css"`再加入另一外部css檔
**"屬性: 值"** 稱做宣告，一則宣告可一次設定多個值
實際顯示順序依據[[選擇器]][[權重]]
因每個瀏覽器顯示的html標籤樣式不同，為了顯示一致的樣式，可先進行[[CSS歸零]]