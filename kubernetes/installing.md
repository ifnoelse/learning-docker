# 安装 Kubernetes

## 基本环境

| 软件名称        | 版本           |
| ------------- |:-------------:|
| centos      | 7.4.1708 |
| docker      | 1.12.6   |
| kubernetes      | 1.5.2 |
| flannel      | 0.7.1    |
| etcd      | 3.2.7    |

## 服务信息
| 服务器名称       | ip           |
| ------------- |:-------------:|
| node-01      | 192.168.100.101 |
| node-02      | 192.168.100.102 |
| node-03      | 192.168.100.103 |

## 主节点安装

### 软件安装
* 安装 kubernetes
``` bash
yum install -y kubernetes
```

* 安装 etcd
``` bash
yum install -y etcd
```

* 安装 flannel
``` bash
yum install -y etcd
```
### 参数配置

* 配置 kubernetes

| 服务名称       | 功能描述          |
| ------------- |:-------------:|
| kube-apiserver      |  |
| kube-controller-manager      |  |
| kube-scheduler      |  |
