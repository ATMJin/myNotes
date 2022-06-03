---
date: 2022-05-16
aliases: [型別列舉]
---
# enum
可將型別存入固定的變數(常數)，如同物件一般，如:
```ts
enum requestStatusCodes {  
  error,  
  success,  
}
enum Season {
  spring,
  summer,
  autumn,
  winter
}
```
也可將變數另外設定值
```ts
enum requestStatusCodes {  
  error = 400,  
  success = 200,  
}
enum Season {
  spring = '3-5',
  summer = '6-8',
  autumn = '9-11',
  winter = '12-2'
}
```
>若不自訂，預設由0開始

使用時直接如物件般使用
```ts
const handleResponseStatus = (status: number): void => {
  switch (status) {
    case requestStatusCodes.success:
      // Do something...
      break;
    case requestStatusCodes.error:
      // Do something...
      break;
    default:
      throw (new Error('No have status code!'));
  }
};
```
或是將變數宣告型別
```ts
let season:Season = Season.spring;
switch (season) {
  case Season.spring:
    // Do something...
    break;
  case Season.summer:
    // Do something...
    break;
  default:
    throw (new Error('No have status code!'));
}
```

