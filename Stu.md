## **学习笔记：**

**kubnernetes目前云服务提供商：**

阿里 ACK，
腾讯TKE，
百度CCE，
AMAZON EKS，
Google GKE，
IMB Cloud K8s，
微软AKS，
CloudStack，
OpenShift，

**Docker的三个基本概念：**

DockerFile（配置文件）：
Image（镜像）：
Container（容器）：

K8s集群的主要组件：

APIserver：
Cloud Controller：
Controller Manager：
Etcd：
Kubelet：
Kube-Proxy：
Scheduler：
Control Plane：
Node：

**安装Docker**


**Git是什么？**

在开发中，Git已成为现在主流的一种代码托管技术，基本上大多数的公司都在使用Git进行协同开发。很多代码托管平台也是基于Git来实现的。此文我们只简单介绍Git的基本使用。
它有什么用？

**Git有什么功能？**

Git里面主要包含的几个概念有远程仓库，克隆，本地仓库，分支，提交，拉取，合并，推送等。


**以前版本控制系统有哪些？**

比如CVS，Subnersion，Mecurial，Perforce，Bazaar等

**Git常用命令：**

1.配置用户信息

`$git config --global  user.name (用户名)`

`$git config --global  user.emial (邮箱)`

2.创建一个仓库

`$git init`

3.从远程服务器克隆仓库

`$git clone (远程仓库的URL)`

4.显示当前等工作目录下提交文件状态

`$git status`

5.将指定文件Stage（标记为被提交等文件）

`$git add （文件路径）`

6.将指定文件Unstage(取消标记为将要被提交的文件)

`$git reset （文件路径）`

7.创建一个提交提供提交信息

`$git commit -m "提交信息"`

8.显示历史提交

`$git log `

9.向远程仓库推送（Push）

`$git push`

10.从远程仓库拉取（Pull）

`$git  pull`

Git学习网站：https://git-scm.com/docs 
