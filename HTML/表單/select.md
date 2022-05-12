下拉式選單，選項使用子元素\<option>，如:
```html
<select>
  <option value="1">選項一</option>
  <option value="2">選項二</option>
</select>
```
亦可用子元素\<optiongroup>做選項分群，如:
```html
<select>
  <optiongroup label="alphabet">
    <option value="1">AAA</option>
    <option value="2">BBB</option>
  </optiongroup>
  <optiongroup label="number">
    <option value="3">111</option>
    <option value="4">222</option>
  </optiongroup>
</select>
```