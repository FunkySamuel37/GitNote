
## 基本操作
---

### 做版本控制
* 做版本控制
```
git add .
git add README.md
```

* 本次提交的注释为 "balabala"
```
git commit -am "balabala"
```
### 小技巧
* 同步远程的版本控制列表，在每次提交前使用
```
git fetch origin
```
* 查看历史版本
```
git log 
```

### 本地版本操作
* 跳转版本
```
git checkout 3ece436886222a106ae34877f9f569162ccb5421 
```
* 回到上一个版本（当未创建分支时）
```
git checkout .
```
* 删掉上一个版本
```
git revert HEAD
```
* 更改版本名
```
git checkout -b first 
```

### 本地分支操作
* 查看分支
```
git branch
```
* 删除本地分支
```
git branch -D TestBranch 
```
* 创建分支
```
git branch beta
```

### 远程分支操作

* 从本地beta 推到远程beta分支
```
git push origin beta:beta
git push origin beta
```
* 删掉远程分支beta
```
git push origin :beta
=
git push origin --delete beta
```
* 强制从远程origin/master分支 覆盖本地TestBranch分支
```
iOSdev git:(TestBranch) git reset --hard origin/master 
```
* push到远程的beta
```
git push origin beta
```
* 强制推到远端//不推荐使用
```
git push --force
```

### remote匹配相关
* 设置一个名为 MasterZhiWei的remote 
```
git remote add MasterZhiWei https://github.com/FunkySamuel37/TestBranch.git
```
* push 到remote MasterZhiWei 下的master分支(远程为空仓库切未初始化)
```
git push MasterZhiWei master
```
* 查看本地配置过的remote列表
```
git remote -v
```

* local push 到 remote ，之后local push时都匹配至remote
- `git push origin local:remote`
- `git push`
