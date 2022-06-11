---
date: 2022-06-10
aliases: [NgModule]
---

# @NuModule

```ts
@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    AppRoutingModule
  ],
  exports: [],
  providers: [],
  bootstrap: [AppComponent]
})
```

一個 NgModule 裝飾器可設定的內容如下:

-   declarations
    這個模組內有哪些元件，若不在此宣告則無法在相同模組得其他元件中使用。
-   imports
    引入的其他模組，除了在裝飾器內宣告外也要在檔案最上面先 import 引入
-   exports
    哪些元件可被引出。也可宣告其他模組名稱，則可使用該模組被公開的元件。
-   providers
    定義模組內各種令牌所使用的提供者清單，以便可以替換掉注入至元件的服務實體????
-   bootstrap
    只能在根模組內設定，定義用來替換`index.html`內`<app-root>`的根元件內容
