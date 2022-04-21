## **学习笔记：**


**kubnernetes：组件说明**

大规模部署分布式应用的平台，管理众多节点或者主机，每个节点运行若干个pod，

Pod是Kubernetes可部署的最小执行单元， Pod运行着web，DB等

control Plan是来控制Pod，专用API与节点进行通讯，检测状态，平衡负载，临时下发指令

Replica Set是副本集合，随时准备切换，保证应用不间断运行

[Pod/Control Plan/Replica Set] 统称为Cluster集群

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

**kubnernetes：环境准备**

1。购买服务器，搭建环境

2。使用现有的云服务提供商

3。Minikube 本地模拟Kubernetes集群

***kubnernetes*目前云服务提供商：**

阿里 ACK，
腾讯TKE，
百度CCE，
AMAZON EKS，
Google GKE，
IMB Cloud K8s，
微软AKS，
CloudStack，
OpenShift，

**本地模拟器环境演示：**

**minikube介绍：**

minikube is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.
What you’ll need

**配置要求：**

2 CPUs or more
2GB of free memory
20GB of free disk space
Internet connection
`官方地址：https://minikube.sigs.k8s.io`

1。安装命令

`%curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-arm64`

`%sudo install minikube-darwin-arm64 /usr/local/bin/minikube`

`% minikube start`
![6Ev1Pl](https://linuxsec.oss-cn-shanghai.aliyuncs.com/uPic/04/6Ev1Pl.png)
------------------------------------------------------------------------
------------------------------------------------------------------------

**Docker**
**1。什么是docker？**

轻量级虚拟机，应用程序的代码，工具库，运行环境都封装到一个容器，降低测试和部署到难度.
（docker /Docker dwarn /podman）轻量级容器
之前为了模拟同样开发环境，用的虚拟机，需要模拟硬件，比如：
（Vmware VirtalBox Hyper-V QEMU ） 运行整个操作系统，臃肿庞大，影响性能。
和虚拟机不同的docker不再模拟硬件，而是给每个应用提供了完全隔离的运行环境。

**2。Docker三个基本概念：**
 
DockerFile（配置文件）：DockerFile自动化脚本，创建镜像。
Image（镜像）：虚拟机的一个快照，包含部署的应用和所有关联库
Container（容器）：通过镜像可以创建不用的Container容器

**3。安装使用**

`Docker Desktop ：https://www.docker.com/get-started/`

Vscode 安装Docker扩展，dockerfile的代码高亮，语法检查，自动补全，菜单运行Dokcer命令
启动docker 

 `% docker run -d -p 80:80 docker/getting-started`


**4。如何用docker compose管理多个容器？**

$docker  compose up -d





------------------------------------------------------------------------
------------------------------------------------------------------------

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
