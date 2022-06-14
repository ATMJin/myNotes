---
date: 2022-06-10
aliases: []
tags: [angular]
---

# Angular 資料結構

src 資料夾內最外層有當作表層容器的`index.html`及核心的程式`main.ts`，`main.ts`內再引入核心的[[Angular模組]]`app.module`，再由`app.module`內引入所需要的[[Angular元件]]。
`index.html`內直接使用標籤`<app-root>`即可替換內容，Angular 在打包時會再自行加上`<script>`
`<app-root>`替換的內容是根模組設定的根元件。
