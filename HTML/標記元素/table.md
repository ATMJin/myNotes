表格，搭配子元素標籤\<tr>\<td>使用，使用\<caption>加入table的標題，如
```html
<table>
  <tr>
    <td>x1,y1</td>
    <td>x2,y1</td>
	</tr>
  <tr>
    <td>x1,y2</td>
    <td>x2,y2</td>
  </tr>
</table>
```
呈現如下

|x1,y1|x2,y2|
|-----|-----|
|x1,y2|x2,y2|

亦有標籤\<th>代表標題、\<thead>代表表首、\<tbody>代表表格內容、\<tfoot>代表表尾，如
```html
<table>
  <thead>
    <tr>
      <th>標題1</th>
      <th>標題2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>x1,y1</td>
      <td>x2,y1</td>
    </tr>
    <tr>
      <td>x1,y2</td>
      <td>x2,y2</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>表尾1</td>
      <td>表尾2</td>
    </tr>
  </tfoot>
</table>
```

|標題1|標題2|
|-----|-----|
|x1,y1|x2,y2|
|x1,y2|x2,y2|
|表尾1|表尾2|

合併儲存格使用屬性rowspan及colspan，如
```html
<table>
  <tr>
    <td>x1,y1</td>
    <td>x2,y1</td>
	</tr>
  <tr>
    <td colspan="2">x1,y2</td>
<!--<td>x2,y2</td> -->
  </tr>
</table>
```

