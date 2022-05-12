---
date: 2021-11-28
aliases: [emmet, 快速輸入]
---
# Emmet快速輸入
- 使用Tab鍵將HTML標籤快速轉換成完整的HTML元素
- 按下Tab時游標要在最後方
- 基本上與CSS[[選擇器]]寫法相同
- [官網全部縮寫一覽](https://docs.emmet.io/cheat-sheet/)
## 標籤
- 單一標籤直接輸入
``` html
  div --> <div></div>
```
- 大於>建立子元素
```html
  div>h1 --> <div><h1></h1></div>
```
- 加號+建立弟元素
```html
  div>h1+p -->
  <div>
    <h1></h1>
    <p></p>
  </div>
```
- 上箭頭(指數符號)^跳到上一層
```html
  div>h1+p^div -->
  <div>
    <h1></h1>
    <p></p>
  </div>
  <div>
  </div>
```
- 乘號* 重複次數
```html
  div*3 -->
  <div></div>
  <div></div>
  <div></div>
  
```
- 小括號( )包裹槽狀結構
```html
  (nav>ul>li*3)+(article>h1+p) --> 
  <nav>
    <ul>
      <li></li>
      <li></li>
      <li></li>
    </ul>
  </nav>
  <article>
    <h1></h1>
    <p></p>
  </article>
      
```
- div可省略，但不能完全沒東西
```html
  >h1 --> X
  []>h1 --> <div><h1></h1></div>
  .class --> <div class="class"></div>
```
## 屬性
- 小數點.添加class，井字號#添加ID
```html
  div.class#id -->
  <div class="class" id="id"></div>
```
- 中括號[ ]輸入屬性
```html
  a[href="#" style="text-decoration: none;"]  -->
  <a href="#" style="text-decoration: none;"></a>
```
## 計數
- 錢號$計數
```html
  li#id$*3 --> 
  <li id="id1"></li>
  <li id="id2"></li>
  <li id="id3"></li>
```
- 小老鼠@設定起始值
```html
  li#id$@7*3
  <li id="id7"></li>
  <li id="id8"></li>
  <li id="id9"></li>
```
- 小老鼠加減號@-降冪
```html
  li#id$@-*3 --> 
  <li id="id3"></li>
  <li id="id2"></li>
  <li id="id1"></li>
  li#id$@-7*3
  <li id="id9"></li>
  <li id="id8"></li>
  <li id="id7"></li>
```
## 內容
- 大括號{ }輸入內容
```html
  p{lorem} -->
  <p>lorem</p>
```
## CSS
- 一般使用屬性及屬性值開頭即可縮寫
```css
m0 --> morgin: 0;
p10p20p --> padding: 10% 20%;
fl --> float: left;
fz16 --> font-size: 16px;
bd3-s#3 --> border: 3px solid #333;
```
