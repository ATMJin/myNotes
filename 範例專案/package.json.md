---
date: 2022-06-14
aliases: []
tags: [node]
---
# package.json
## script
### `node --max_old_space_size=12288 ./node_modules/@angular/cli/bin/ng serve`

最前面`node --max_old_space_size=12288`設定node使用的最大記憶體，單位MB。
因為有時候在起專案時會超出node的預設記憶體大小，所以設大一點避免錯誤。

後面`./node_modules/@angular/cli/bin/ng serve`指訂由專案文件內的angular來執行。
因為開發者電腦內的angular版本可能與專案使用的版本不一致。