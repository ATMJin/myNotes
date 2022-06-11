---
date: 2022-06-11
aliases: []
---

# @Component

```ts
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
```

@Component 裝飾器常用的屬性有以下:

-   selector
    元件被使用時的名稱，格式是 "前字元 + 元件名稱"
-   templateUrl
    元件的 html 模板檔案路徑。
    若為元件內模板，則使用 telplate 屬性且屬性值用字串直接寫 html。
-   -styleUrls
    元件的 css 檔案路徑。
    若為元件內樣式，則使用 styles 屬性，並使用字串陣列。單一字串或多字串皆可。
