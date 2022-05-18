---
date: 2022-01-22
aliases: []
---
# v-on
增加事件監聽
`v-on:事件="Vue中的函式或運算式"`
可簡寫成
`@事件="Vue中的函式或運算式"`

## [[事件物件]]
若無指定傳入參數時，可在函式中直接使用事件物件。
但若有其他參數時，需另外傳入`$event`來指定事件物件。

## 修飾符

### .stop
阻擋事件冒泡

### .prevent
取消元素預設行為，如submit的傳送或a的連結

### .capture
設定事件以捕獲的形式觸發

### .self
只觸發元素本身的事件，不觸發由冒泡或捕獲傳來的世間。

### .once
事件只觸發一次。

### .passive
設定元素不會被取消預設事件。
因為一般情況下，觸發事件後瀏覽器會檢查是否有設定preventDefault；在譬如scroll事件下會連續觸發事件而連續進行判斷，進而影響效能。
`.passive`與`.prevent`互觸，`.passive`優先於`.prevent`。

## 判斷輸入的修飾符

### 鍵盤修飾符
可直接指定要監測哪個按鍵被按到，如:
- .enter
- .esc
- .tab
- .space
- .delet (包括delet鍵與backspace鍵)
- .up
- .down
- .left
- .right
- .alt
- .shift
- .ctrl
- .meta (windows鍵或mac的command鍵)
- .page-up (複合名稱要使用聯字號)
- .page-down
> keycode(如數字13代表enter鍵)已從正式網頁標準被移除，故在 Vue 3 不支援。

### 滑鼠修飾符
判斷滑鼠點擊鍵
- .left
- .right
- .middle (中鍵)

### .exact
只有在正確的按鍵下才會觸發事件。
譬如只有設定單一space鍵會觸發事件，但使用者同時按下 crtl + space 也會觸發，這時加上`.exact`可避免此情況。