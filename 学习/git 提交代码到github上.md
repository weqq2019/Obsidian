---
layout: post
title:  "git 提交代码到github上"
categories: [开发工具,git]
tags:  git
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/u=3808378362,2299808617&fm=26&gp=0.jpg
---

* content
{:toc}
# 小总结一下命令:
git pull 获取新版本

git status

git add .

git commit -m "add new files"

git push -u origin master




# git 提交代码步骤

利用命令行提交代码步骤
提交代码之前，需先从服务器上面拉取代码，以防覆盖别人代码。
## 1：拉取服务器代码
git pull
## 2：查看当前工作目录树的工作修改状态
git status
状态：
1：Untracked: 未跟踪, 此文件在文件夹中, 但并没有加入到git库, 不参与版本控制. 通过git add 状态变为Staged.
2：Modified: 文件已修改, 仅仅是修改, 并没有进行其他的操作.
3：deleted： 文件已删除，本地删除，服务器上还没有删除.
4：renamed：

## 3：将状态改变的代码提交至缓存
git add + 文件
git add -u + 路径：将修改过的被跟踪代码提交缓存
git add -A + 路径: 将修改过的未被跟踪的代码提交至缓存
例如：
git add -u vpaas-frontend/src/components
将 vpaas-frontend/src/components 目录下被跟踪的已修改过的代码提交到缓存中

git add -A vpaas-frontend/src/components
将 vpaas-frontend/src/components 目录下未被跟踪的已修改过的代码提交到缓存中

## 4：将代码提交到本地仓库中
git commit -m “注释部分 ref T3070”

注：
T3070： 任务号

## 5：将代码推送到服务器
git push

问题
1：误将代码提交到缓存中（利用 git add 命令误将代码提交的缓存中）
解决办法：利用 git reset 命令将撤回缓存中的代码。

2：误将代码提交到本地仓库（利用 git commit 命令误将代码提交到本地仓库）
解决办法：
git reset —soft + 版本号
回退到某个版本，只回退了commit的信息，不会改变已经修改过的代码。
git reset —hard + 版本号
彻底回退到某个版本，本地的代码也会改变上一个版本内容。



