---
date: 2024-05-10
aliases:
  - 觀察者
  - 訂閱者
tags:
  - RxJS
---
# Observer

用來處理 [[Observable]] 發出的新數據。通常有以下三種:

- next: 用於處理 Observable 發出的下一個數據。
- error: 錯誤處理。
- complete: 當 Observable 完成發出所有數據時。