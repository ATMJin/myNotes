## \<[[div]]>  
單純的區塊、容器，無語意

## \<section>
章節、段落、彼此有相關的內容

## \<article>
文章、獨立存在也無影響的文章

使用上如:
```html
<article>
  <h1>Heading</h1>
  <section>
    <h2>Section heading 1</h2>
    <p>content</p>
  </section>
  <section>
    <h2>Section heading 2</h2>
    <p>content</p>
  </section>
  <section>
    <h2>Section heading 3</h2>
    <p>content</p>
  </section>
</article>
```
建議在使用時就算內容沒需要，也加入標題並隱藏，以增加SEO
註: 隱藏元素會降低SEO。

section、article、[[nav]]、[[aside]]屬同一層級章節元素。