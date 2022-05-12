---
date: 2021-12-02
aliases: []
---
可放在[[script]]標籤中，或其他標籤內。
在連結[[a]]標籤中的寫法如:
```html
<a href="javascript:windows.alert('Hello World')"></a>
```





|載入script的方式|script類型|時序|使用時機|
|--------------|---------|--|-------|
|`<script>`放在`<body>`的任意位置|inline/file|瀏覽器讀取到script標籤後HTML中斷，待載入、解析、並執行程式碼後再繼續HTML|功能單純，對頁面渲染影響不大的小程式|
|`<head>`中加入`<link rel="preload" as="script">`|file|載入頁面時下載並解析，在HTML建立完後執行|進行頁面操作和前端功能實做的主程式|
|`<script>`加入`defer`屬性|file|讀到script標籤後載入程式碼，同時繼續HTML，在HTML建立完後解析並執行|進行頁面操作和前端功能實做的主程式|
|在`<script>`加入`type="module"`屬性值|inline/file|讀到script標籤後載入程式碼及相關模組，在HTML建立完後解析並執行|將進行頁面操作和前端功能實做的主程式模組化引入|
|在`<script>`加入`async`屬性|file|讀到script標籤後載入程式碼，同時繼續HTML。程式碼下載完後中斷建立HTML，優先解析執行JS|希望下載後立即執行，並且對頁面渲染影響不大的程式|
|在`<script>`同時加入`type="module"`及`async`|file|讀到script標籤後載入程式碼及相關模組，下載完後中斷建立HTML，優先解析執行JS|希望下載後立即執行，並且對頁面渲染影響不大的模組化程式|