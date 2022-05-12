获得或设置元素的 DOM 属性

## class操作
* .addClass('class')  向匹配的元素添加指定的class名。
* .removeClass('class')  从所有匹配的元素中删除全部或者指定class。
* [[toggleClass('class')]]  對取得的元素，如有( )內的Class值時，刪除該值；若無則添加。
* .hasClass('class')  检查匹配的元素是否拥有指定的class。

## 元素
- .prepend(元素)  插入子元素，已有子元素時插入最前方 
- .append(元素)  插入子元素，已有子元素時插入最後方 
- .remove()  刪除元素

## 屬性
- .attr('屬性名稱')  讀取元素屬性的值
- .attr('屬性名稱','值')   在元素中設定屬性與屬性值
- .removeAttr('屬性')  从所有匹配的元素中移除指定的属性。

## 文字
- .text('')   讀取文字內容
- .text('文字')   替換改寫文字


* .html()  设置或返回匹配的元素集合中的 HTML 内容。

* val()  设置或返回匹配元素的值。