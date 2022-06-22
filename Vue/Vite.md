---
date: 2022-05-12
aliases: []
tags: [vue]
---

# Vite

Vue 官方取代 Vue-CLI 的 Vue3 建構工具

## 建立方法

建立一個新的 Vite 專案的方法為
```sh
npm create vite@latest 
```
或
```sh
pnpm create vite
```
或
```sh
yarn create vite
```


將 vite 改成 vue 在創建時可選擇更多選項


## vite.config 配置

### 變更輸出資料夾

```js
build: {
  outDir: "./docs",
}
```

### 取消編譯後的亂數

```javascript
build: {
    rollupOptions: {
        output: {
            entryFileNames: `assets/[name].js`,
            chunkFileNames: `assets/[name].js`,
            assetFileNames: `assets/[name].[ext]`
    }
},
```