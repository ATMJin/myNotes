---
date: 2022-01-07
aliases: [LIKE]
---
# 字元模糊比對
```sql
LIKE "pattern" [ESCAPE "character"]
```

## pattern
要比對的字元，其中
- % 代表有字元或沒字元
- 底線_  代表有一個字元

如`LIKE "ABC"`意思為字元要完全符合"ABC"；`LIKE "%ABC%"`為字串裡有"ABC"，在最前面或最後面都可以；`LIKE "_ABC"`代表第二個字元開始要是"ABC" 

## ESCAPE
設定跳脫字元
譬如%與_ 皆有代表的意思，所以設定跳脫字元使兩者可以被查詢，如
```sql
LIKE "%ABC\%\%\%" ESCAPE "\"
```
意思為設定反斜線\為跳脫字元，\%是%字元，所以要搜尋結尾是ABC%%%的字串。