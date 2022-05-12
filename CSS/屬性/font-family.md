- 使用時直接輸入內建字體，如`font-family: "標楷體"`
- 或從[Google字型](https://fonts.google.com/)連結網路字體使用
- 或使用字型檔，利用@font-face加入。方法為:
```css
@font-face {
  font-family: "自訂名稱";
  src: url(字型檔路徑)
}

p {
  font-family: "自訂名稱";
}
```
- 須考慮字型檔大小，若檔案太大下載速度慢，影響使用者體驗
  - 可加入`font-display: swap`使網頁先載入預設字型
- 如要用粗體，最好另外設定粗體字型