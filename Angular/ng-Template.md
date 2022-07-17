---
date: 2022-07-17
aliases: []
tags: [angular]
---

# ng-Template

可用來存放一段 HTML ，並且不會被渲染出來。並在需要時插入指定的地方。
必須將其取名，這樣才能在使用時知道要用哪個 ng-template。

```html
<ng-template #sample>
  In template.
</ng-template>
```

可利用 `*ngTemplateOutlet` 指令來使用需要的 ng-template

```html
<div *ngTemplateOutlet="sample"></div>
```


也可傳入參數，如:
```html
<ng-template #sample let-myName="name">
  My name is {{myName}}.
</ng-template>

<div *ngTemplateOutlet="sample; context: {name: 'Jin'}"></div>
```

或是用 $implicit 設定預設參數

```html
<ng-template #sample let-myName>
  My name is {{myName}}.
</ng-template>

<div *ngTemplateOutlet="sample; context: {$implicit: 'Jin'}"></div>
```