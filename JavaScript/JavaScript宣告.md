使用let、var、const來進行宣告。
宣告過的變數跨script標籤也可使用。
const為不變的常數值，與let同屬區塊宣告。
let的範圍為當前區塊(大括號)，如迴圈、函式等，必須先宣告再使用，且不可重複宣告。
var則作用在所有範圍，且瀏覽器會先配置記憶體給所有var宣告後再置入值，因此可使用後在後行再宣告。
因此建議使用let進行宣告，增加嚴謹性，避免重複宣告。

變數必須使用字母（letter）、下底線（\_）、錢號（$）作為開頭

```js
let string = "string"  ///後面為字串直接宣告成字串
let number = 1234.5678   //數字number不區分整數小數，實際為雙精度浮點數
let boolean = true   //布林值true跟false
let null = null  
let undefined = undefined  
/*null與undefined顯示上一樣是沒有值，null == undefined，但null !== undefined
null是被定義的沒有值，型態是object；undefined是未定義或不存在，型態是undefined*/

//另有一種變數型態symbol，用來表示獨一無二 (unique) 的值(?)
```