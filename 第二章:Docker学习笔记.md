
Docker学习笔记

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

