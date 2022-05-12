---
date: 2022-01-10
aliases: []
---
基本樣式為`$('選擇器')`，取得所有符合選擇器的元素
除了可以使用[[選擇器|CSS選擇器]]外，也有JQ特有的篩選器(Filter)，長相類似[[偽類別|偽類]]

## 基本順序篩選器
- :first
- :last
- :odd
- :even
- :eq(index)
- gt(index)
- lt(index)

## 內容篩選器
- :empty
- :parent  找非空元素
- :contains(string)
- selector1:has(selector2)
- selector1:not(selector2)

## 可視篩選器
- :visible
- :hidden 所有看不見的元素，包含`display:none;` `visibility:hidden;` `<input type="hidden">`

## 表單相關篩選器
- :input  同`<input>`
- :text  同`<input type="text">`，以下同
- :password
- :radio
- :checkbox
- :reset
- :submit
- :button
- :file
- :image
- :hidden
- :checked
- :selected
- :disabled
- :enabled
- :focus

## 其他篩選器
- :header  標題如h1
- :lang(語言)
- :animated  在執行動畫的元素
- :root  `<html>`
- :target

## this
$(this)