---
date: 2022-07-12
aliases: []
tags: [angular, Material]
---

# Material Divider

Material 風格的分隔線，看起來跟 [[hr]] 差不多，只是顏色是搭配 Material 風格的淺灰色。

使用前必須先引入
`import {MatDividerModule} from '@angular/material/divider';`

使用 `<mat-divider>` 標籤

可綁定兩種屬性
- `[inset]="true"` 會產生 margin-left: 80px; 的內縮
- `[vertical]="true"` 文件寫垂直線，但實際沒實驗出來。