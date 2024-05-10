---
date: 2024-05-10
aliases: 
tags:
  - RxJS
---
# Creation Operators

又被稱作創建操作符，專門用於創建 [[Observable]]，而不是對現有的 Observable 進行轉換或處理。
可以單獨存在。
有以下:

1. **ajax：** 用於創建 Observable，以發送 Ajax 請求並將其結果轉換為 Observable。
2. **bindCallback：** 將回調式的 API 轉換成 Observable。
3. **bindNodeCallback：** 將 Node.js 風格的回調 API 轉換成 Observable。
4. **defer：** 當有訂閱時才創建 Observable，以便每次訂閱都有一個新的 Observable。
5. **empty：** 創建一個立即完成的 Observable，不發出任何值。
6. **from：** 接受類陣列、Promise、可迭代對象、Observable-like 對象或者一個可處理可迭代對象的函數作為參數，並將它們轉換為一個發出相應數據的 Observable。
7. **fromEvent：** 監聽 DOM 事件並創建一個對應的 Observable。
8. **fromEventPattern：** 創建一個 Observable，該 Observable 使用提供的訂閱和解除訂閱函數來監聽事件。
9. **generate：** 創建一個 Observable，該 Observable 根據提供的初始狀態、條件和迭代器生成值。
10. **interval：** 創建一個每隔指定時間間隔發出自增數字的 Observable。
11. **never：** 創建一個永遠不會發出任何值或完成的 Observable。
12. **of：** 接受一個或多個值作為參數，並將這些值轉換為一個發出這些值的 Observable。
13. **range：** 創建一個發出指定範圍內連續整數的 Observable。
14. **throwError：** 創建一個立即拋出錯誤的 Observable。
15. **timer：** 創建一個在指定延遲後發出單個值的 Observable，或在延遲後開始定期發出值。