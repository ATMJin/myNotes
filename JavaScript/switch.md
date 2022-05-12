```js
let key = 100

switch (key) {
  case 100 :
    console.log("這是100")
    break;
  case 200:
    console.log("這是200")
    break;
  case 300:
    console.log("這是300")
    break;
  default:
    console.log("都不是")
    break;
}

```

switch (運算式) {  case 指定值:  執行 ; [ break;]   }
直接判斷是否符合case的值，為嚴格判斷，1不等於"1"
如果不加break會依序往下執行其他case，直到break或switch結束。