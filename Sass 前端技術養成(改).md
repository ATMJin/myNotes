
# Sass 前端技術養成

讓你寫css時不再重複
> 以下程式碼標註SCSS的有些是SACC，因為Obsidian會有問題
---

# Sass 環境安裝

- ### 先安裝node.js

 https://nodejs.org/en/

- ### 全域安裝 Sass

 終端機：`npm install sass -g`

---
# 為何要學sass

1. Sass是"Syntactically Awesome StyleSheets"的簡稱 ，
簡單說就是 css 預處理語言

2. Sass讓編寫可維護的Scss，更簡易方便。
可以用多餘的時間，做更多的事。

---
## Sass 資源

- sass 中文官網 https://sass.bootcss.com/

- sass 英文官網 https://sass-lang.com/
--- 

## sass 與scss不同處

- 副檔名不同，寫法都不同，兩者不能兼容
- scss 可以兼容css的寫法

取決於副檔名 `.sass` 與`.scss`

https://sass-lang.com/guide
---
```scss
//sass語法
$width: 200px
.box
    width: $width


//Scss語法
$width: 200px;
.box {
    width: $width;
}
```
---
- ### sass / scss 語法
```scss
// Sass語法
=cover
  $color: red
  @for $i from 1 through 5
    &.bg-cover#{$i}
      background-color: adjust-hue($color, 15deg * $i)
.wrapper
  +cover
  
// Scss 
@mixin cover {
  $color: red;
  @for $i from 1 through 5 {
    &.bg-cover#{$i} { background-color: adjust-hue($color, 15deg * $i) }
  }
}
.wrapper { @include cover }  
```
--- 
# sass 編譯指令

### style.scss -> style.css
`sass style.scss style.css`
### 監看檔案變動
`sass style.scss style.css --watch`

---
# 編譯工具介紹 

1. 線上編譯工具 : https://www.sassmeister.com/
2. VsCode 編譯工具 : [live sass compile](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)

---

## Vscode  設定css 輸出

設定css 輸出的資料夾，在檔案<喜好設定<設定
![](https://i.imgur.com/6klXVRK.png)

---

 -> 搜尋找到seeting.json檔案，放入底下這段，
可以改編譯過後的路徑。

 #### setting.json
 ```json
//css產出設定
 "liveSassCompile.settings.formats": [
        {
            "format": "expanded", //壓縮成一行"compressed", //壓縮成一行css，正式版本
            "extensionName": ".css",
            "savePath": "/css/" //此為輸出的路徑，可以自行更改
        }
    ],
 
 ```
---
# $變數
---

# 變數命名方式
Sass / Scss 變數的宣告主要依靠 `$` 關鍵字，
```scss
  $a = 10;
  $fontSize = 20px;
```

---

# 數值型態

- 數值 (Number)：12、100px (可能有或沒有單位)
- 字串 (String)：Microsoft JhengHei (可能有或沒有引號)
- 顏色 (Color)：blue、#4cb5fc、hsl(204, 97%, 64%)
- 列表 (List)：1px 2px 3px 1px(中間可空格或是 用 , 區隔)
- 地圖 (Maps)：(primary: blue, danger: red)
- 布林 (Boolean)：true、false
- 空值 (Null)：null

---

 官方文檔函式參考 (Function references)：
https://sass-lang.com/documentation/values 

---

### 變數型態
```scss
// 變數型態
$font_size-h1 : 50px; //數值
$font_color: rgb(255, 81, 0); // 顏色
$margin : 10px 20px 30px 40px; //  list
$null : null; //空值
$if : true //判斷式
$bg-color : (
  'blue' : #0059ff,
  'yellow' : #ffd900,
  'green' : #73ff00
); 
// map 數值
```

---

## 變數管理技巧
- 1. 變數會先宣告，所以要放在檔案最上方
- 2. 把介面共用的參數設定為變數
```scss
//字體
$fontSize :  16px;
$fontWeight: 400;
//顏色
$Body_color: #999;
$body_BgColor : #fff;
```
---

-  3.變數命名方式通常以屬性的名稱來命名，要有語義化。
-  4.區域變數與全域變數(只要在`{}` 裡的通常為**區域變數**)

```scss
//全域變數
$width: 100px


//區域變數
.box {
 $width: 100px //區域變數
 width: $width;
}
```

## 字串轉換
如果你想在一个字串是使用一个變數，簡單來说，就是使用 `#{}` 来包裹這個變數。

只要在  **url路徑 / class 名稱 / 屬性名稱**  都需要使用**字串轉變數**

---

## 顏色函式

明亮度Darken & Lighten 調整
```scss
lighten($color, $amount)
darken($color, $amount)
```

https://sass-lang.com/documentation/modules/color




---

# 運算子與條件判斷式



---

### 比較符號

```
$a == 10    
$a >= 10   
$a =< 10  
$a != 10
並沒有 ===

```

<br>
<br>

---

### 判斷式
```
@if $a { 如果是$a 條件成立執行 }

@else if $b {如果$a 不成立，執行這段}

@else {以上條件都不成立，就執行這段}

```

---

###  運算子

```scss
//注意 “單位” 跟 “除法”
.box {
    width: 10px + 5px; //單位相同，可以相加
    height: 10px - 5;
    max-width: 10 * 10px; //單位相同不能相乘
    min-height: (50px / 20); //除式要()
    font: 12px / 18px; // font-size / line-height
}
```

<br>
<br>

---

###  運算函式
```scss
 floor(14.58px); // 14px 無條件捨去 
 width: round(14.58px); // 15px 四捨五入
 height: ceil(14.38px); // 15px 無條件進位
```
<br>
<br>


---

### 條件

1.  and：兩個運算式都是 true 時才會回傳 true
2. or：兩個運算式有任一個是 true 時就會回傳 true
3. not 反轉運算式結果
```scss
@if $a == #000 and $a == black {}
```
<br>
<br>

---

# Nesting 巢狀寫法

讓 css 可讀性更高


---

### 使用nesting的黃金規則：

1. nesting永遠不要超過三個層級
2. 確保輸出的CSS簡潔、可重用
3. 使用nesting是很有意義的，而不是默認選項

```scss
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
    
    li { 
      display: inline-block; 
       }
  }
}
```
---


### 輸出
```css=
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav ul li {
  display: inline-block;
}
```

---

## 偽元素 &

css
```css=
/*scss如何寫*/
a:hover { color:#333}
p::after {content : ''}

```

scss
```scss
a {
  &:hover {color: #333}
}

p {
  &::after { content : ''}
}
```
--- 



#  @import   輸入 sass檔案
讓sass 重組檔案

<br>
<br>


---


### _files.scss  不會編譯成為 css

路徑 ： assets/sass/_var.scss;

```scss
//使用 @import 把檔案連結進來

@import 'path/file'

@import 'assets/sass/var '
```

<br>
<br>

---

# @Mixin 函式 

@mixin 讓我們定義可重複使用的樣式。
@include 可以將呼叫（mixin）到文檔中。

---


## @mixin基本寫法

```scss=
@mixin margin-auto() {
    margin-left: auto;
    margin-right: auto;
}

.box {
  @include margin-auto();
}

```

### 輸出
```css=
.box {
    margin-left: auto;
    margin-right: auto;
}

```


---

## 變數搭配使用

```scss=
//宣告
@mixin rect($width , $height: $width) {
    width: $width;
    height: $height;
}

//呼叫
.box {
   @include rect(100px)
}

```

### 輸出
```css=
.box {
     width: 100px;
     height: 100px;
}

```

---

## 在函式裡時，變數 null值 跟 預設值


1. 當變數為null值時，可以不帶值
2. 變數為預設值時，不帶值時，會帶預設值進去

---

```scss
// mixin 帶值  // 預設值 // null值
@mixin rect($w, $h:$w, $bgc:null) {
  width: $w;
  height: $h;
  background-color: $bgc;
}
```
### 輸出
```css=

.box {
@include rect(10px , 20px , #333)    // #333 這值可以不帶入
}

```





---

## @mixin裡在呼叫另一個函式

```css=
@mixin margin-auto() {
    margin-left: auto;
    margin-right: auto;
}

@mixin rect($width , $height: $width) {
    width: $width;
    height: $height;
    //可以呼叫另一個函式
    @include  margin-auto()
    
}

```


---

## @mixin + @content 擴增屬性 

```scss
@mixin btn-module($class, $w , $p , $align:center) {
    #{$class} {
       width: $w;padding: $p 0;
       text-align: $align; 
       @content; //擴增屬性
    }
}
```

---

## 使用方式

```scss
@include btn-module(.a ,100px , 20px  , center){
   // 擴增屬性
   border: 1px soild #333;
}
```
---


# Sass 迴圈介紹
for/ each / while 迴圈

---

## @for 迴圈
```scss
// start 起始值->end結束值
@for $i from Start through End {
   .box-#{$i} {
     width : $i * 1px
   }
}
```
---
```scss
// for 迴圈
@for $i from 1 through 10 {
    .box-#{$i} {
        width: $i * 1px;
    }
}
```
---

## 輸出

```css=
.box-1 {
  width: 1px;
}

.box-2 {
  width: 2px;
}
......

```



練習
https://www.sassmeister.com/


---



### grid system

```scss
@mixin grids($key, $num) {
 @for $i from 1 through $num {
   .col-#{$key}-#{$i} {
     width: floor(($i / $num) * 100%);
     @content  }}};

// grid
@include grids(md , 12);
```
### 輸出

練習: https://www.sassmeister.com/

---


# $map 數值型態 


---


### $map

[sass-map 用法出處](https://sass-lang.com/documentation/values/maps)

通過閱讀一些文章，覺得Sass的map是Sass的強大的特性之一，能幫助我們做好更多的事情，比如說管理媒體查詢的斷點、管理z-index的值、管理顏色和管理排版等。接下來，我們一起來學習Sass的map。


---

```scss=
 $map : (
   key : value,  
   key1: 10px,
   key2: 20px,
   key3: 30px,
   key4: 40px,
   key5: 50px
 )

```
``` scss=
map-get($map,$key)：根據給定的key值，返回map中相關的值。
map-merge($map1,$map2)：將兩個map合併成一個新的map。
map-remove($map,$key)：從map中刪除一個key，返回一個新map。
map-keys($map)：返回map中所有的key。
map-values($map)：返回map中所有的value。
map-has-key($map,$key)：根據給定的key值判斷map是否有對應的value值，如果有返回true，否則返回false。
keywords($args)：返回一個函數的參數，這個參數可以動態的設置key和value。
```

---


## @each 用法

```scss
@each $var in $list {
   
   .box_#{$var} {
      // option
   }
} 
// $var 內部變數  
// $list 外部傳遞
```
---

```scss
@mixin img_module ($list) {
        @each $man in $list {
            .photo-#{$man} {
                background:url('images/#{$man}.jpg');
                @content;
            }
        }
    }
```

### 使用方法
```scss
@include img_module(a1 a2){
    background-repeat: no-repeat;
    background-size: cover;
};
```
---

### 輸出

css

```css=
.photo-a1 {
  background: url("images/a1.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}

.photo-a2 {
  background: url("images/a2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}

```

---



# 參考資料

[sass官網中文文檔](http://sass.bootcss.com/docs/sass-reference/)
[sass官網英文文檔](https://sass-lang.com/)


# 專題參考資源
1. https://getbootstrap.com/docs/4.3/layout/grid/
2. https://biings.design/#/
3. https://autoprefixer.github.io/