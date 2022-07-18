---
date: 2022-06-13
aliases: []
tags: [angular]
---

# \*ngFor

類似 Vue 的 [[v-for]] ，可依據陣列或物件重複渲染
基本語句為
```html
<div *ngFor="let item of items"></div>
```

## 變數

除了陣列或物件中取出的值外，也有內建一些變數
- index 索引值
- first 是否為第一項
- last 是否為最後一項
- even 是否為偶數項
- odd 是否為奇數項
其中除了 index 是整數值外其餘皆是布林值。

使用時可以先用 `let` 宣告一個新變數再去使用。
```html
<div *ngFor="let item of items; 
     let recordIndex = index; 
     let firstRecord = first; 
     let lastRecotd = last; 
     let evenRecord = even; 
     let oddRecord = odd">
</div>
```


## ngFor

帶星號的 ngFor 實際為一個語法糖，最後會轉換成 ng-template

```html
<div *ngFor="let item of items"> {{ item }} </div>
<!-- 轉變成 -->
<ng-template ngFor let-item [ngForOf]="items">
  <div> {{ item }} </div>
</ng-template>
```