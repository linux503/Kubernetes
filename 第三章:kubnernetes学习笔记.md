kubnernetes学习笔记


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