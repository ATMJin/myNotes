---
date: 2022-06-14
aliases: []
tags: [angular, angularCLI]
---

# ng serve
建立可在本地電腦執行的虛擬伺服器

## 參數

### --host
設定要配置的伺服器位置，字串型別，預設localhost
--host=0.0.0.0，在相同區網下使用區網ip可連到架專案電腦

### --live-reload
是否及時更新畫面，布林值，預設true

### --aot
是否使用預先(ahead-of-time)編譯器，布林值，預設true
> 從 Angular 9已經將預先編譯器做為預設，可在 angular.json 內調整設定
> 所以此已為廢棄參數

### --configuration
選擇建構器使用何種命名配置，命名配置由 angular.json 的 configurations 屬性設定。

### --proxy-config
設定 proxy 的配置檔案



