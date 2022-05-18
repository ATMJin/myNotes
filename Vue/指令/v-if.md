
---
date: 2022-01-22
aliases: []
---
# v-if
寫在標籤內，v-if="陳述式"
如果v-if內的值為[[falsy value|falsy]]，則不存在(物件不存在，不會被Vue渲染出來)。

> 在Vue 2 時，當 v-if 和 [[v-for]] 同時使用時， v-for 優先度更高；
> 在Vue 3 ，v-if 優先於 v-for；
> 因此避免錯誤，==官方強烈建議避免 v-if 與 v-for 寫在同一標籤。==

## v-else v-else-if
v-if 的後續邏輯判斷，接續前一個 v-if。
若有連續要使用 v-else，可用 div 或 template 標籤包裹。

## key
> Vue 2 會產生的問題，在Vue 3 已被修正。

Vue 會重複利用元素，因此在某些情況下用 v-if v-else 切換時，原本輸入框裡的值會殘留。
這時在不同的input內加入不同屬性值的key屬性(不限於被綁定的:key)即可被認做不同元素被渲染。