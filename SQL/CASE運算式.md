---
date: 2022-01-07
aliases: [CASE]
---
將值依條件做比較後再回傳指定值
```SQL
CASE column
  WHEN v1 THEN r1
  [WHEN v2 THEN r2]
  ...
  [ELSE r3]
END
```
or
```SQL
CASE
  WHEN 條件1 THEN r1
  [WHEN 條件2 THEN r2]
  ...
  [ELSE r3]
END newColumnName
```