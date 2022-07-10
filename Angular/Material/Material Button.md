---
date: 2022-07-10
aliases: []
tags: [angular, Material]
---

# Material Button

Material 樣式的 Button ，要先引入`MatButtonModule`，
`import {MatButtonModule} from '@angular/material/button';`

只需在`button`標籤和`a`標籤加入指定的指令即可改變標籤的外觀。

- `mat-button` 基本的樣式，純文字帶透明底
- `mat-raised-button` 比較像傳統的按鈕，有陰影形成立體感
- `mat-stroked-button` 文字加灰色邊框
- `mat-flat-button` 帶背景顏色的扁平樣式
- `mat-icon-button` 純icon無背景的按鈕，可搭配 [[Material Icon]]
- `mat-fab` 有背景顏色和陰影的中等大小圓，可搭配 Material Icon
- `mat-mini-fab` 較小的`mat-fab`，可搭配 Material Icon


顏色可使用 Material 預設的樣式設計，分為三種，primary、accent、warn
在標籤內加入 `color="warn"` 使用。
