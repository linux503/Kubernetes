Git学习笔记

Git是什么？

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

`%docker ps` 查看所有容器 

`%docker stop id`  停止容器

`%docker restart id` 重启容器

`%docker rm id` 删除容器

`%docker exec -it  id  /bin/bash` 启动一个远程shell

**4。如果要保存docker 数据？**

`volume 数据卷`（本地主机不同容器之间的共享文件夹）

`% docker volume create my-data`  创建数据卷

` docker run -dp 80:5000  -v my-data:/etc/data  id` -v可以启动的时候选择数据库卷
**5。如何用docker compose管理多个容器？**

多容器应用独立运行可以做到数据应用的有效分离

`%docker  compose up -d` 运行所有容器

`%docker compose down` 停止并删除所有容器

`%docker compose down --volumes` 停止并删除所有容器和数据卷

**6。docker和kubernetes的区别和联系？**

docker正在被kubernetes取代？其实值得是kubernetes中的容器引擎而已，因为二者不是一个层面的东西。

kubernetes主要应用在集群环境，主要提供负载均衡，故障转移。
kubernetes所做的是将各个容器分发到一个集群上运行，并进行全自动管理，包括部署和升级。

 **最后关于细节部分可以在docker中文指南查看**：
` https://yeasy.gitbook.io/docker_practice`




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
