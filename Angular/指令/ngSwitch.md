---
date: 2022-07-11
aliases: []
tags: [angular]
---

# ngSwitch

類似 Vue 的 v-switch。
依據判斷綁定的變數內容決定渲染哪個DOM

```html
<div [ngSwitch]="conditionExpression">
    <div *ngSwitchCase="expression">output</div>
    <div *ngSwitchDefault>output2</div>
</div>
```