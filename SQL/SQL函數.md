---
date: 
aliases: [Function]
---
## 字串函數
- **CONCAT(expr1, expr2, ...)**  將資料作為字串結起來，資料可以是任意型態
- LENGTH(str)  字串長度(回傳Byte)
- CHAR_LENGTH(str)  字元數量
- LCASE(str) 轉小寫
- LOWER(str) 同上
- UCASE(str)  轉大寫
- UPPER(str)  同上
- ASCII(str)  回傳ASCII碼
- FIELD(str, str1, str2, ...)
- INSERT(str, pos, len, newstr)
- LEFT(str, len)
- RIGHT(str, len)
- REVERSE(str)
- LPAD(str, len, padstr)
- RPAD(str, len, padstr)
- SUBSTRING  擷取字串
- REPEAT
- SPACE
- INSTR
- LOCATE
- REPLACE
- LTRIM
- RTRIM
- TRIM
- STRCMP

## 數值函數
- ROUND(x, d)  四捨五入
- TRUNCATE
- MOD
- CEIL
- FLOOR
- POWER
- SQRT
- ABS
- SIGN
- RAND
- PI()  圓周率
- RADIANS  度轉徑
- DEGREES  徑轉度

## 日期時間函數
- **CURDATE**
- CURTIME
- CURRENT_TIMESTAMP
- **NOW**
- UTC_DATE
- UTC_TIME
- UTC_TIMESTAMP
- **YEAR**
- MONTH
- DAY
- HOUR
- MINUTE
- SECOND
- TIME
- MICROSECOND
- EXTRACT
- DAYNAME
- MONTHNAME
- DAYOFWEEK
- DAYOFMONTH
- DAYOFYEAR
- WEEK
- **WEEKDAY**
- WEEKOFYEAR
- YEARWEEK
- **DATEDIFF**
- **ADDDATE**
- SUBDATE
- ADDTIME
- SUBTIME
- TIMEDIFF
- TIMESTAMP
- TIMESTAMPADD
- TIMESTAMPDIFF
- PERIOD_DIFF
- DATE
- STR_TO_DATE
- MAKEDATE
- MAKETIME
- **DATE_FORMAT**
- TIME_FORMAT
- TO_DAYS
- FROM_DAYS
- LAST_DAY
- QUARTER
- TIME_TO_SEC
- SEC_TO_TIME

## 資料型態轉換函數
- CAST
- **CONVERT**

## 通用函數
### 系統資訊函數
- USER( )  連線的使用者
- VERSION( )  資料庫版本
- DATABASE( )  連線的資料庫
- CONNECTION_ID( )  連線的Connection ID
- CHARSET(str)  字串所屬的字元集
### 流程控制函數
- IFNULL(expr1, expr2)
- IF(expr1, expr2, expr3)
- NULLIF(expr1, expr2)

## 匯總/群組函數
- COUNT(\*)
- COUNT(column)
- COUNT(DISTINCT column)
- MAX(column)
- MIN(column)
- SUM(column)
- AVG(column)