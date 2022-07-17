---
date: 2022-07-17
aliases: []
tags: [angular]
---

# Input

接收從父元件傳來的值
寫法為:

```html
<!-- 父元件 Parent.html 內 -->

<app-child [PropertyA]="value"></app-child>
```

```ts
// 子元件 Child.ts 內

import { Input } from '@angular/core';

export class ChildComponent {
  @Input PropertyA
}
```