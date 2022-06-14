---
date: 2022-06-14
aliases: []
tags: [angular]
---

# Angular服務元件

在 Angular 中，一般元件應只負責展示畫面，而無處理資料邏輯。
處理邏輯拆出成服務元件。

在 [[Angular CLI]] 建立服務元件的方式為
```sh
$ ng generate service 元件名稱
```
亦可縮寫成
```sh
$ ng g s 元件名稱
```