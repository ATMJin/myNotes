- \<ruby> 文字旁註記，如注音、假名、音標等，搭配子元素\<rt>、\<rp>
- \<rt> 放在ruby內的基礎文字後，內加注音
- \<rp>  包住\<rt>，給不支援ruby文字的瀏覽器使用

範例:
```html
<ruby>約束された勝利の剣<rt>エクスカリバー</rt></ruby>
<ruby>超電磁砲<rp><rt>Railgun</rt></rp></ruby>
```