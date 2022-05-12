- placeholder  輸入框底下呈現的內容，不會消失
- value 欄位預設值
- readonly  唯讀
- disabled  不可使用
- name  將眾多input視為一組，如radio及checkbox。若使用在checkbox，建議名稱後加入中括號
- checked  預設已勾選欄位，如使用在radio及checkbox
- autofocus  自動聚焦，網頁讀取完成時自動將輸入位置聚焦該欄位
- autocomplete  自動完成
- required  必填欄位
- pattern  利用正則表示式來限制使用者輸入的內容
- list  將某datalist與輸入欄位連結，list屬性值需與datalist元素值ID相同
  -> 範例
  ```  html
  <datalist id="Alphabet">
    <option value="AAA">AAA</option>
    <option value="BBB">BBB</option>
    <option value="CCC">CCC</option>
  </datalist>
  <input type="text" list="Alphabet">
  ```
- multiple  可輸入多個值
- novalidate  回傳的資料不會被檢核，只能用在form
- fornovalidate  回傳的資料不會被檢核，可用在submit
  -> 如:
  ```html
  <form action="process.php">
    <label for="email">EMAIL:</label>
    <input type="text" name="email" value="@gmail.com">
    <input type="submit" value="submit" formnovalidate>
  </form>

  <form action="process.php" novalidate>
    <label for="email">EMAIL:</label>
    <input type="text" name="email" value="@gmail.com">
    <input type="submit" value="submit">
  </form>
  ```
- form  
- formaction
- formenctype
- formmethod
- formtarget
