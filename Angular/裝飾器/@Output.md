---
date: 2022-07-17
aliases: []
tags: [angular]
---

# @Output

可在建立一個 EventEmitter 泛型型別後利用 emit() 方法將值作為事件物件參數 $event 傳送致父元件。
如:

``` ts
export class ChildComponent implements OnInit {
  // @Output()裝飾器 表示這是一個要輸出的事件
  @Output() outputAddHero = new EventEmitter<any>() 
  inputDefaultHero: string = "myName"

  constructor() { }

  addHero() {
    this.outpuftAddHero.emit(this.inputDefaultHero)
  }
}
```

```html
<app-child (outputAddHero)="getNewHeroFromAnotherComponent($event)">
</app-child>
```

```ts
getNewHeroFromAnotherComponent(newHero){ 
// 資料以參數的形式傳送出來，同樣也要以參數的形式接住
    console.log(newHero)
}
```
