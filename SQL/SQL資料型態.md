---
date: 2022-01-06
aliases: []
---
## 字串
- **CHAR(n)**  固定長度字元，最大長度n，不足以空白填入，n值從0~255
- **VARCHAR(n)**  可變長度字元，尾部空白保留。值從0~65535
- TEXT  分大小寫
  - TINYTEXT
  - TEXT
  - MEDIUMTEXT
  - LONGTEXT
- BLOB  Binary，照片或音樂檔等，不分大小寫
  - TINYBLOB
  - BLOB
  - MEDIUMBLOB
  - LONGBLOB

## 數值
### 浮點數
- **DECIMAL[(p[,s])]**  數值資料，儲存時以字串儲存，p為總長度，s為小數位數，即(p-s).s
- **NUMERIC**  同DECIMAL
- FLOAT
- DOUBLE

### 整數
- **INT(n)**  整數
  - TINYINT  1Byte
  - SMALLINT  2Bytes
  - MEDIUMINT  3Bytes
  - INT  4Bytes
  - BIGINT  8Bytes

## 日期
- DATE  日期"yyyy-mm-dd"
- **DATETIME**  日期時間，格式為"yyyy-mm-dd hh:mm:ss"
- TIMESTAMP  同DATETIME，使用UTC儲存，依所在地時區顯示，且因使用4bytes，時間範圍只有1970年~2038年
- TIME   "hh:mm:ss"
- YEAR
### 日期格式
"yyyy-mm-dd hh:mm:ss"
"YYYYMMDDHHMMSS"
年可只後兩碼，引號可省略