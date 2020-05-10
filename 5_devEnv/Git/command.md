# Git 版本管理

1. Git 是如何管理版本分支的？

## Git 分为四个区

- Workspace：工作区

- Index：暂存区

- Repository：本地仓库

- Remote：远程仓库

## 命令

### 工作区代码如何提交到远程仓库

工作区提交到暂存区

> git add .

暂存区提交到本地仓库

> git commit -m 'message'

本地仓库提交到远程仓库

> git push

### 远程仓库代码如何拉到本地

一. 获取整个项目

新建代码库

> git init 'project-name'

下载一个项目

> git clone url

二. 获取项目更新的分支

下载远程仓库的所有变动

> git fetch

获取远程仓库的信息，拿到 remote

> git remote -v

本地仓库新建分支

> git checkout -b 'branch-name'

获取远程分支，与本地仓库合并

> git pull 'remote' 'branch'

### 本地分支如何推送到远程

本地新建分支，跳转到该分支

> git checkout -b 'branch-name'

推送本地分支到远程仓库

> git push 'remote' 'branch'

备注： 如果本地有该分支，远程没有。需要在本地分支和远程分支之间建立关联 ，origin 替换成库的链接

git push --set-upstream origin 5_devEnv

### 合并分支

切换到 master 分支

> git checkout -b 'master'

合并 branch-A 到 master 分支

> git merge branch-A
