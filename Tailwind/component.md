---
date: 2022-07-11
aliases: []
tags: [tailwind]
---

# Tailwind Component

## 創建方式

在最外層 style.css 中，使用
```css
@tailwind components;

@layer components {
  .classname-by-self{
    @apply tailwind-css-class
  }
}
```