.toggleClass("class")  對取得的元素，如有( )內的Class屬性值時，刪除該值；若無則添加。
語法:
```js
$(selector).toggleClass(class,switch)
```
若class有多項，用空格格開
switch非必要，用來控制只添加或刪除，為布林值

如
```js
$("button").click(function(){
  $("p").`toggleClass("main")`;
})
```
則
```html
<p class="">   <--->   <p class="main">
```
