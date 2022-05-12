# 連結或下載
## 連結
1. 搜尋[Google CDN](https://developers.google.com/speed/libraries)
2. 將裡面的程式碼(`<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>`)直接複製貼上至html內
## 下載
1. 進入https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js 
2. 另存為js檔

# 使用
``` html
<script>
$(document).ready(function() {
    jQuery程式碼;
})
</script>
```
or
``` html
<script>
jQuery(document).ready(function() {
    jQuery程式碼;
})
</script>
```
or
``` html
<script>
$(function() {
    jQuery程式碼;
})
</script>
```

意思為，當HTML讀取完畢後，執行function