---
updatedate: 2021-12-17 
aliases: []
---
查詢裝置的長寬及解析度等

```css
@media (條件) and (條件如最小寬度min-width) { 符合件要執行的CSS }
如
@media screen and (min-width: 768px) {
  body {
    background-color: #000;
  }
}
/* 螢幕 and 最小寬度768px(>=768px) 時，背景黑色。 */
```
如果有多個查詢時，條件較嚴的寫在條件寬的後面，如min-width: 810px 寫在min-width:360px後面。因為後條件會覆蓋前條件。