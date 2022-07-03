# Angular 概述

嗨~如果你是很注重架構及團隊Team Work的人且如果專案避不開功能切分開發元件化，很推薦你使用Angular。Angular已經是一套非常成熟的平台框架，他是以HTML與TypeScript去建置客戶應用端平台。在使用Angular以前會建議你對裝飾者及依賴注入有些微了解，這樣使用起來才會較得心應手。因為畢竟偏向開發大型專案用，所以架構上會較嚴謹。

## [Angular需要瞭解區塊](https://hackmd.io/@spyua/B1hZD3D8O#Angular需要瞭解區塊 "Angular需要瞭解區塊")

-   1.Command Line
-   2.File Architecture
-   3.DataBinding
-   4.Grammar
-   5.Module
-   6.Components
-   7.Directives
-   9.Pipes
-   10.Services
-   11.Routing

## [1. Command-Line](https://hackmd.io/@spyua/B1hZD3D8O#1Command-Line "1Command-Line")

Angular在新增專案、檔案以及安裝套件上完全使用Command Line模式去執行。故需對ng基礎指令需有了解，詳述可看官網連結。

## [2. File Architecture](https://angular.tw/guide/file-structure)

![](https://i.imgur.com/bXGH80H.png)

| 檔案 | 說明 |
| -------- | -------- | 
| src     | 所有專案主要開發的原始程式碼，以及透過 Angular CLI 所產生的檔案，都會存放在這個目錄下     |
| src/app     | 放置整個網頁開發中，所需要的程式邏輯、資料、樣式、測試，以及 Angular 的元件(Component)、模版(Template)、模組(Module)、服務(Service)。     |
|src/app/app-routing.module.ts|設定 Router(路由器)；指當瀏覽器的 URL 發生變化時，Router(路由器)會依據查詢到的對應 Route(路由)來決定顯示哪個元件。 |
|src/app/app.component.css |根元件 AppComponent 的樣式檔(CSS) |
|src/app/app.component.html |根元件 AppComponent 的 HTML 範本檔 |
|src/app/app.component.spec.ts |根元件 AppComponent 的單元測試定義檔。 |
|src/app/app.component.ts|根元件 AppComponent 的主程式 |
|src/app/app.module.ts|AppModule 的根模組，為應用程式的 NgModule 定義檔； 每當你於專案中，新增元件(Component)時，該檔案將會自動新增宣告該項元件(Component)。 |
|assets/|放置網站影像和靜態資源檔案(Image、CSS、Fonts...)。 |
|environments/ |放置環境變數的設定檔；專案建立時，預設會有一個無名的標準開發環境(environments.ts)和一個生產(“prod”)環境(environments.prod.ts)  |
|environments/environments.ts | 標準開發環境變數設定檔(production：false。 |
|environments/environments.ts |生產環境變數設定檔(production： true)。 |
|favicon.ico |出現在瀏覽器網址列、書籤、頁籤的小 icon 圖檔。 |
|index.html |預設為網站首頁，也是 SPA 唯一一頁。 |
|main.ts |整個網頁應用程式的主要切入點，用於 Angular CLI 編譯與打包時。 |
|polyfills.ts | 為瀏覽器支援提供了膩子（polyfill）指令碼，載入 Angular 程式之前，會預先加載完成。|
|style.css | 整個網站共用的 CSS 樣式檔。|
|test.ts |單元測試的主入口點；通常不需要編輯這個檔案。 |


## [4.DataBinding](https://angular.tw/guide/binding-syntax)

目前前端三大框架都已使用MVVM Pattern，有別與傳統MVC，在資料面的部分使用資料繫結。在資料變動後，View會動態跟著變動。

[資料繫結有四種方法](https://ithelp.ithome.com.tw/articles/10219733)

-   1.  字串插植
    -   直接在 Template 中插入 `{{value}}`，執行期間 value 的變化，都會連動更新到 Template 畫面上。
-   2.  屬性綁定
    -   在 HTML 中的屬性加入 `[property]="value"`，執行期間 value 的變化，會值接影響 property。
-   3.  事件綁定
    -   在 HTML 中的加入 `(event)="functionName()"`，當發生指定 event 時，就會呼叫 TypeScript 中的 functionName 方法。
-   4.  雙向綁定
    -   在 HTML 中的加入 `[(ngModel)]="value"`。雙向綁定用於可以讓使用者互動的 HTML 元素，如：、、…等。

![](https://i.imgur.com/O0m7IEv.png)


## [5.Grammar](https://angular.tw/guide/built-in-directives)

-   屬性指令
    -   用來改變視圖元件的 “外觀和行為”，例如預設的背景色、滑過改變顏色，常用的指令如 NgStyle。
        -   NgClass —— 新增和刪除一組 CSS 類別。
        -   NgStyle —— 新增和刪除一組 HTML 樣式。
        -   NgModel —— 將資料雙向繫結新增到 HTML 表單元素。
-   結構指令
    -   用來修改視圖的 “結構”，例如添加或移除DOM布局，常用的指令如 NgIf 和 NgFor。
        -   NgIf —— 從範本中建立或銷燬子檢視。
        -   NgFor —— 為列表中的每個條目重複渲染一個節點。
        -   NgSwitch —— 一組在備用檢視之間切換的指令。


## [6.Module](https://angular.tw/guide/architecture-modules)

一個 Module ( 模組 ) 是一個把彼此互相關聯的 components、directives、pipes 和 services 整合的機制。然後這個模組可以再和其他模組結合，最後就形成我們的網頁應用程式。網頁就像拼圖一般，由許多小碎片的組件和一塊一塊的模組所構成。

![](https://i.imgur.com/R00qGqL.png)

-   import：預期有一個陣列包含要引入的所有陣列。
-   declaration：預期有一個陣列包含所有這個模組要用的 components、directives 和 pipes。
-   bootstrap：我們用來定義根組件 (root component)，雖然可以是一個陣列，但通常我們只會定義一個而已。根組件會再引入其他更多的組件。


## [7.Components](https://angular.tw/guide/component-overview)

Angular 的介面呈現主要是透過元件(Component)來構成與處理，而元件需依附於模組(NgModule)。而一個 Module ( 模組 ) 是一個把彼此互相關聯的 components、directives、pipes 和 services 整合的機制。然後這個模組可以再和其他模組結合，最後就形成我們的網頁應用程式。網頁就像拼圖一般，由許多小碎片的組件和一塊一塊的模組所構成。

-   每個元件包括如下部分
    -   .html : 一個 HTML 範本，用於宣告頁面要渲染的內容
    -   .ts : 一個用於定義行為的 Typescript 類別
    -   .css :一個 CSS 選擇器，用於定義元件在範本中的使用方式

例子，圖中局框處設計為一個List Component，顯示格式排版一樣內容物不同。  
![](https://i.imgur.com/IMRMRXn.png)


## [8.Directives](https://angular.tw/guide/attribute-directives)

屬性指令(Attribute directives) : 用來改變視圖元件的"外觀和行為"，簡單來說就是自建HTML Tag元件，透過裝飾者模式直接掛載到現有專案Module 上。例如預設的背景色、滑過改變顏色，常用的指令如NgStyle。[範例](https://lawrencetech.blogspot.com/2017/06/angular-directive.html)


## [9.Pipes](https://angular.tw/guide/pipes)

資料進行轉換和格式化使用。

-   現有Pipe功能
    
    -   DatePipe：根據本地環境中的規則格式化日期值。
    -   UpperCasePipe：把文字全部轉換成大寫。
    -   LowerCasePipe ：把文字全部轉換成小寫。
    -   CurrencyPipe ：把數字轉換成貨幣字串，根據本地環境中的規則進行格式化。
    -   DecimalPipe：把數字轉換成帶小數點的字串，根據本地環境中的規則進行格式化。
    -   PercentPipe ：把數字轉換成百分比字串，根據本地環境中的規則進行格式化。
-   [自製Pipes](https://ithelp.ithome.com.tw/articles/10187136)
    


## [10.Services](https://angular.tw/guide/architecture-services)

Services簡單來說就是提供應用所需的函示或數值處理，在這邊除了函式邏輯處裡外大部分指得是API呼叫。在Angular新增服務也是透過下CLI:ng new service指令新增，當使用CLI下完新增Serice指令後，CLI會自動幫你把DI相關設置好，在ts檔就可直接注入所新增的Service服務函示。


## [11.Routing](https://angular.tw/tutorial/toh-pt5)

一個Angular的應用程式中只會有一個Routing，當瀏覽器的URL更改時，router會尋找Route裡確認要顯示的組件及畫面。要使用Route，要將Router透過RouterModule.forRoot做配置並且將添加到AppModule的imports陣列。