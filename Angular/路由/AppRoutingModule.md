---
date: 2022-07-01
aliases: []
tags: [Angular]
---

# AppRoutingModule

用 Angular CLI 建立專案選擇加入路由時，Angular 預設的路由模組，會引入 angular 的 [[RouterModule]] 來使用路由功能。
基本內容為

```ts
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';

const routes: Routes = [ ];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule],
})
  
export class AppRoutingModule { }
```

基本 routes 路徑設定的方式為:

```ts
const routes: Routes = [
  { path: '路徑', component: 要顯示的Component, }
];
```

設定好後即可用 [[RouterLink]] 建立連結及用 [[RouterOutlet]] 切換顯示 Component。
或是在 ts 中使用 [[Router 類型]] 

## 萬用路由 (wildcard route) 

```ts
{
  path: '**',
  component: 要顯示的Component,
}
```
任何路徑都會導向指定 Component 
如果設在路徑設定的最前面，會無法連到其他路徑。
