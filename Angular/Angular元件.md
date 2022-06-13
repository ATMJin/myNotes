---
date: 2022-06-10
aliases: []
tags: [angular]
---

# Angular 元件

## 建立方式

在 Angular CLI 中，可利用指令建立元件

```sh
$ ng generate component 元件名稱 [參數]
```

或是使用縮寫

```sh
$ ng g c 元件名稱 [參數]
```

會直接建立四個檔案，html、css、ts 及測試用的`.spec.ts`檔
建立完後會自動將元件加入至最近模組的 declarations 屬性內

### 參數

使用 Angular CLI 指令建立元件時輸入的參數常用的有:

-   --inline-template (-t) / --inline-style (-s)
    可將頁面模板與樣式都放在元件內，類似 Vue 的 SFC，而非各自單獨檔案
-   --prefix (-p)
    設定元件名稱的前面字元，如`app-root`前面的`app`。
-   --skip-selector
    省略 [[@Component]] 裡面的 selector 屬性。
-   --module (-m)
    專案有複數模組時，指定元件是哪個模組的。
-   --export
    自動將元件名稱加入所屬模組的 [[@NgModule]] 的 exports 屬性內。
