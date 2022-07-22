---
date: 2022-07-22
aliases: []
tags: [angular]
---
# @ViewChild

會在檢視的 DOM 中查詢能匹配上該選擇器的第一個元素或指令。 如果檢視的 DOM 發生了變化，出現了匹配該選擇器的新的子節點，該屬性就會被更新。

若後面類型指定為 ElementRef 即可操作頁面上的 HTML 元素
```html
<div #hello>Hello World</div>
```
```ts
@ViewChild("hello") elRef: ElementRef;

console.log("ElementRef", this.elRef.nativeElement.innerText);
// Hello World
```



