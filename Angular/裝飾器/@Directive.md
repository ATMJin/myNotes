---
date: 2022-07-18
aliases: []
tags: [angular]
---

# @Directive

定義指令在使用時的名稱

```ts
@Directive({
  selector: "[appHellowWorld]"
})
export class HelloWorldDirective{}
```

中括號代表指令是以屬性的方式使用。

前面也可加上 HTML 標籤，代表只能用在指定標籤，如:
```ts
@Directive({
  selector: "div[appHellowWorld], button[appHellowWorld]"
})
export class HelloWorldDirective{}
```