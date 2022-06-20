---
date: 2022-06-20
aliases: []
tags: [git]
---
# 基本 git 操作指令

基本終端機操作指令同Linux，如ls、cd、pwd、rm......等
一開始要對欲進行管理的資料夾進行初始化，輸入`git init`
查看當前專案版本，`git log`
顯示哪些檔案被更動但未更新，`git status`
新增/更新檔案，`git add`
專案版本更新，`git commit`，後方可加入`-m "版本更新說明"`
推上github，`git push`
第一次從github拉下來，`git clone`
之後拉下來，`git pull`
建立分支，`git branch`
查看目前所在分支，`git branch
切換分支，`git checkout

設定個人資料
``` git
git config --global user.name "姓名"
git config --global user.email "Email"
```
查詢設定，`git config --list`，按q退出
