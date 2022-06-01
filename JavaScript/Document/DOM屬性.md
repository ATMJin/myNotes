---
date: 2022-01-10
aliases: []
---
適用[[document]]內的節點(node)
## 描述層級關係
- parentNode
- childNodes
- firstChild
- lastChild
- previousSibling
- nextSibling

|     JS    |     jQ     |
|-----------|------------|
|parentNode |$().parent()|
|childNodes |$().children()|
|firstChild |$().first() |
|lastChild  |$().last()  |
|previousSibling|$().prev() or $().prevAll()|
|nextSibling|$().next() or $().nextAll()|

## 描述本身的資訊
- nodeType
- nodeValue
- nodeName