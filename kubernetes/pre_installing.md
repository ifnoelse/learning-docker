# 安装前的准备

* 准备服务器

| 服务器名称       | ip           | 操作系统           |
| :-------------: |:-------------:|:-------------:|
| node-01      | 192.168.100.101 |centos-7.4.1708|
| node-02      | 192.168.100.102 |centos-7.4.1708|
| node-03      | 192.168.100.103 |centos-7.4.1708|
| node-04      | 192.168.100.104 |centos-7.4.1708|

* 按照以上计算算计明修改对应节点的hostname

``` bash
echo "计算机名称">/etc/hostname
```

* 配置 /etc/hosts
``` bash
for i in {1..4};do echo "192.168.100.10${i}	node-0${i}">>/etc/hosts;done
```

* 关闭防火墙
``` bash
systemctl disable firewalld
systemctl enable docker
```

* 关闭 selinux
``` bash
setenforce 0
sed -i 's/SELINUX=permissive/SELINUX=disabled/g' /etc/selinux/config
```

* 禁用 IPv6
``` bash
sysctl -w net.ipv6.conf.all.disable_ipv6=1
sysctl -w net.ipv6.conf.default.disable_ipv6=1
echo "net.ipv6.conf.all.disable_ipv6 =1">>/etc/sysctl.conf
echo "net.ipv6.conf.default.disable_ipv6 =1">>/etc/sysctl.conf
```