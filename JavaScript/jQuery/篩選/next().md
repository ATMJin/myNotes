.next()  前面選擇器取得元素的下一個弟元素
如
``` html
<div class="submenu">
 <h3>2. How To Use</h3>
 <ul class="hidden">
  <li><a href="">- 基本操作方式</a></li>
  <li><a href="">- 回復至最初狀態</a></li>
  <li><a href="">- 製做外掛工具</a></li>
 </ul>
</div>
 ```
 ``` js
 $(".submenu h3").next()
 取得的元素為<ul>
 ```