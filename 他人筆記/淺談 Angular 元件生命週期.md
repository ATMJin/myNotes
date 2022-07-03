# [學習筆記] 淺談 Angular 元件生命週期


## Angular 的生命週期

> 官方文件：[生命週期鉤子 Lifecycle Hooks](https://angular.cn/guide/lifecycle-hooks)

在 Angular 的每個元件都存在著生命週期（Lifecycle），從建立元件，檢測綁定屬性是否更新，到元件從 DOM 中銷毀，就構成一個元件的生命週期。

而 Angular 提供了八個 Lifecycle Hooks（生命週期鉤子），讓使用者能夠在各個階段對元件進行操作。

舉例來說，當我們建立一個叫做 test 的 Component，就會去呼叫 constructor 和 ngOnInit 來初始化元件：

```
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  templateUrl: './test.component.html',
  styleUrls: ['./test.component.scss']
})
export class TestComponent implements OnInit {

  constructor() { }

  ngOnInit(): void {
  }

}

```

## [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#生命週期鉤子的順序 "生命週期鉤子的順序")

## 生命週期鉤子的順序

> 範例程式碼：[Stackblitz](https://stackblitz.com/edit/angular-lifecycle-hooks-tkbcaf?embed=1&file=app/app.component.ts)

關於 Angular 生命週期鉤子的執行順序，大致排列如下：

![](https://i.imgur.com/2QDkCAe.png)

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#Constructor-建構式 "Constructor-建構式")

### Constructor 建構式

-   constructor() 會在 class（類別）建立時最先被執行
-   是類別的屬性， Angular 並不能控制 constructor
-   當 constructor 執行時，元件尚未被初始化，因此幾乎不會在這個階段寫程式碼
-   主要用於相依注入（dependency injection），例如服務、函式或值

```
constructor(private service: HeroService) { }
```

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#ngOnChanges "ngOnChanges")

### ngOnChanges

-   當元件 @Input/@Output 綁定的值發生變化時觸發
-   在 ngOnInit 之前執行

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#ngOnInit "ngOnInit")

### ngOnInit

-   用來初始化頁面內容，顯示數據綁定、設置 directive 和輸入屬性
-   在第一次 ngOnChanges 完成後呼叫，只執行一次

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#ngDoCheck "ngDoCheck")

### ngDoCheck

-   當狀態發生變化，而 Angular 本身無法檢測該變化時觸發
-   在 ngOnChanges 和 ngOnInit 之後，於每次檢測變化時執行
-   使用時需注意：ngOnChanges 被觸發的頻率非常高，程式碼應盡量精簡，避免導致頁面性能問題

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#ngAfterContentInit "ngAfterContentInit")

### ngAfterContentInit

-   頁面有使用 ng-content 進行元件內容投射
-   在初始化之後會執行一次

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#ngAftertContentChecked "ngAftertContentChecked")

### ngAftertContentChecked

-   在每次檢查投射內容時執行
-   在每次呼叫 ngDoCheck 之後觸發

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#ngAfterViewInit "ngAfterViewInit")

### ngAfterViewInit

-   在元件或其子元件檢視初始化之後，會執行一次

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#ngAfterViewChecked "ngAfterViewChecked")

### ngAfterViewChecked

-   在每次檢視元件或其子元件之後觸發

### [](https://hackmd.io/@Heidi-Liu/angular-lifecycle#ngOnDestory "ngOnDestory")

### ngOnDestory

-   在元件被摧毀之前執行

參考資料：

-   [Angular 完整元件生命週期介紹](https://www.youtube.com/watch?v=-HoKK2KyurQ)
-   [Angular：生命週期和鉤子函數](https://limeii.github.io/2019/06/angular-lifecycle-hooks/)