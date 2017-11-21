# 启动集群

## 启动主节点

### 设置服务开机启动

``` bash
systemctl enable kube-apiserver
systemctl enable kube-controller-manager
systemctl enable kube-scheduler
systemctl enable etcd
systemctl enable flanneld
```

### 启动服务

``` bash
systemctl restart etcd
systemctl restart flanneld
systemctl restart kube-apiserver
systemctl restart kube-controller-manager
systemctl restart kube-scheduler
```

## 启动从节点

### 设置服务开机启动

``` bash
systemctl enable docker
systemctl enable kubelet
systemctl enable kube-proxy
systemctl enable flanneld
```

### 启动服务

``` bash
systemctl restart flanneld
systemctl restart docker
systemctl restart kubelet
systemctl restart kube-proxy
```

## 查看集群节点

如果安装及配置都正确的话，应该可以通过以下命令查看到集群中的相关节点，在主节点执行以下命令

``` bash
[ifnoelse@node-01 ~]$ kubectl get node
NAME      STATUS    AGE
node-02   Ready     1d
node-03   Ready     1d
node-04   Ready     1d

```
> 管理命令需要在主节点执行