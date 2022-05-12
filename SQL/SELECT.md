---
date: 2022-01-06
aliases: []
---
# 查詢資料
## 子句

|子句(Element)|運算式([[Expression]])|用途(Role)|
|------------|------------------|---------|
|SELECT   |\<select list>     |查詢的資料項目      |
|FROM     |\<table source>    |資料來源           |
|[[#WHERE]]    |\<search [[condition]]>|查詢/過濾資料條件   |
|GROUP BY |\<group by list>   |資料分組設定       |
|HAVING   |\<search condition>|分組資料查詢/過濾條件|
|[[#ORDER BY]] |\<order by list>   |查詢結果排序方式    |


## 語法
```sql
SELECT *|{[DISTINCT] 欄位名稱|運算式 ["欄位別名"] [,...]}
FROM TableName ;
```
expression 算術運算式
SELECT後方除了全部資料(\*)外，也可以使用欄位(Column name)、常值([[Literal]])、運算式([[Expression]])、函數([[SQL函數|Function]])查詢。
SELECT與FROM必填。


### 查詢所有欄位的資料
```sql
SELECT *
FROM TableName ;
```
### 查詢指定欄位的資料
```sql
SELECT Column name[as "別名"] [, another column, ...]
FROM TableName ;
```
## 排除重複的資料(DISTINCT)
```sql
SELECT DISTINCT column
FROM tableName;
```

## LIMIT
限制傳回的資料筆數
```sql
SELECT column
FROM tableName
LIMIT [offset,] count;
```
offset 第幾筆開始，資料筆數從0開始計算，同JS[[陣列]]
count 回傳幾筆

## WHERE
查詢符合條件的row
寫在FROM後面
```sql
WHERE 條件子句(contition)
```
### [[Condition]]

## ORDER BY
將資料排序
ORDER BY子句位置在SELECT敘述區塊的最後一行。
```SQL
SELECT ...
FROM ...
WHERE ...
ORDER BY ...
```
可指定欄位或運算式的資料值來排序。
後方接`ASC`或`DESC`來指定升冪或降冪排列，不寫則為預設升冪ASC。
排序依據可為欄位、別名、運算式、欄位的位置
用逗號(,)分隔，依序排序。

