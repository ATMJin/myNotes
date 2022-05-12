JSON(JavaScript Object Notation)，其內容由屬性和值所組成

JSON的基本資料類型：

-   數值：十進位數，不能有前導0，可以為負數，可以有小數部分。還可以用`e`或者`E`表示指數部分。不能包含非數，如NaN。不區分整數與浮點數。JavaScript用雙精度浮點數表示所有數值。
-   字串：以雙引號`""`括起來的零個或多個[Unicode](https://zh.wikipedia.org/wiki/Unicode "Unicode")[碼位](https://zh.wikipedia.org/wiki/%E7%A0%81%E4%BD%8D "碼位")。支援[反斜槓](https://zh.wikipedia.org/wiki/%E5%8F%8D%E6%96%9C%E6%9D%A0 "反斜槓")開始的[跳脫字元序列](https://zh.wikipedia.org/wiki/%E8%BD%AC%E4%B9%89%E5%AD%97%E7%AC%A6%E5%BA%8F%E5%88%97 "跳脫字元序列")。
-   布林值：表示為`true`或者`false`。
-   陣列：有序的零個或者多個值。每個值可以為任意類型。序列表使用方括號`[]`括起來。元素之間用逗號`,`分割。形如：`[value, value]`
-   物件：若干無序的「鍵-值對」(key-value pairs)，其中鍵是數值或字串。建議但不強制要求物件中的鍵是獨一無二的。物件以花括號`{`開始，並以`}`結束。鍵-值對之間使用逗號分隔。鍵與值之間用冒號`:`分割。
-   空值：值寫為`null`