---
date: 2024-09-22
aliases:
tags:
  - Python
---

# `lambda`

Ptyhon 中的匿名函式，但只支援單行表達式。
若要寫多行邏輯，可以使用普通的函式定義來實現，或是將邏輯包裝成普通函式後再用`lambda`

```python
add = lambda x, y: x + y
print(add(3, 5)) # 8
```

```python
def add(x, y):
  return x + y
print(add(3, 5)) # 8
```
