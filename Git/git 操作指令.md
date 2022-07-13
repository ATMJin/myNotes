---
date: 2022-06-20
aliases: []
tags: [git]
---
# 基本 git 操作指令

基本終端機操作指令同Linux，如ls、cd、pwd、rm......等

- `git init`，對欲進行管理的資料夾進行初始化，開始git版控
- `git log`，查看當前專案版本。
- `git status`，顯示哪些檔案被更動但未更新。
- `git add`，新增/更新檔案。
- `git commit`，專案版本提交更新，後方可加入`-m "版本更新說明"`
- `git push`，推上 github 等網路空間。
- `git clone`，第一次從github拉下來
- `git pull`，之後拉下來
- `git branch`，建立分支
- `git branch`，查看目前所在分支
- `git checkout`，切換分支

設定個人資料
``` git
git config --global user.name "姓名"
git config --global user.email "Email"
```
查詢設定，`git config --list`，按q退出
