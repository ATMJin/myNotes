Math.random()  回傳一個 0 到 1 之間的偽隨機值

如想取得1以上的亂數，可用類似以下寫法，x為預取得數值的上限
```JS
Math.ceil(Math.random()*x)
或
Math.floor(Math.random()*x) + 1
```

如骰子為
```JS
Math.ceil(Math.random()*6)
or
Math.floor(Math.random()*6) + 1
```