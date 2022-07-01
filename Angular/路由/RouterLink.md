---
date: 2022-07-01
aliases: []
tags: [angular]
---

# RouterLink

可在 `<a>` 標籤設定 `routerLink` 指令來建立路由連結。
使用方法為
```html
<!-- 指定字串 -->
<a routerLink="'/'">首頁</a>
<!-- 或綁定文字陣列 -->
<a [routerLink]="['task', 'list']">工作事項</a>
```

## routerLinkActive

```html
<a routerLink="'/'" routerLinkActive="class名稱">首頁</a>
```
類似 [[Vue Router]] 的 `router-link-active` 功能
可在路徑名稱匹配時加入 class ，並由 class 控制外觀。

```html
<a routerLink="'/'" 
   routerLinkActive="class名稱"
   [routerLinkActiveOptions]="{exact: true}">
   首頁
</a>
```

`routerLinkActiveOptions` 類似 Vue router 的 `router-link-exact-active` 
exact 設定為 true 時為精準比對路徑，否則通常只要前面一樣就好。