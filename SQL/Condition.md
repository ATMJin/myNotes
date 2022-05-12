---
date: 2022-01-07
aliases: []
---
# 條件子句
由運算元與運算子組成，運算元可以是欄位、[[Expression|運算式]]、[[SQL函數]]、[[Literal|常值]]
運算元可為任意型態，字串會轉為內碼

## 比較運算子
- 等於 =
- 大於 >
- 大於等於 >=
- 小於 <
- 小於等於 <=
- 不等於 <>

## 邏輯運算子
- AND
- OR
- NOT 同 [[JavaScript運算子#邏輯運算子]]中的!

## SQL特定運算子
- BETWEEN  在指定區間內，包含端點，`x BETWEEN 小數 AND 大數`意思同`x>=小數 AND x<=大數`
- IN  在指定的值內，`x IN (a, b, c)`同`x=a OR x=b OR x=c`
- [[LIKE運算子|LIKE]]  字元比較
- IS NULL  是[[null]]值
    - 用not否定要寫成`IS NOT NULL` 