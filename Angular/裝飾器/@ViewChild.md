---
date: 2022-07-22
aliases: []
tags: [angular]
---
# @ViewChild

會在檢視的 DOM 中查詢能匹配上該選擇器的第一個元素或指令。 如果檢視的 DOM 發生了變化，出現了匹配該選擇器的新的子節點，該屬性就會被更新。

@ViewChild("elRef") elRef!: ElementRef;

console.log("ElementRef", this.elRef.nativeElement);
