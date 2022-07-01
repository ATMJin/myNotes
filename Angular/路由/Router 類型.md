---
date: 2022-07-01
aliases: []
tags: [angular]
---

# Router 類型
由 angular 提供的 Router 類型，需先引入才可使用
```ts
import { Router } from '@angular/router';
```

其中可利用 `navigate()` 或 `navigateByUrl()` 來跳轉指定路徑

```ts
constructor( router: Router ) {}

// navigate 使用字串陣列
this.router.navigate(['task', 'list']);
// navigateByUrl 直接使用字串
this.router.navigateByUrl('task/list');
```

