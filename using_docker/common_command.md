# 常用命令
   
## 查看Docker版本

``` bash
sudo docker version
```

## 镜像操作

* 检索镜像
``` bash
sudo docker search [镜像名称]
``` 
* 下载镜像
``` bash
sudo docker pull [镜像名称]:[TAG]
``` 
* 下载镜像
``` bash
sudo docker pull [镜像名称]:[TAG]
``` 
* 列出已有镜像
``` bash
sudo docker images
```
* 删除镜像
``` bash
sudo docker rmi [镜像ID]
```
* 查看镜像历史
``` bash
sudo docker history [镜像ID]
```
> 默认不能删除有容器依赖的镜像，可以通过参数-f强制删除，强制删除镜像不会删除相关容器

## 启动容器

* 创建一个容器
``` bash
sudo docker run -it [镜像名称]:[TAG] /bin/bash
```
* 启动/停止/重启/删除一个已有容器
``` bash
sudo docker [start/stop/restart/rm] [容器名称/容器ID]
```
* 连接一个已启动的容器
``` bash
sudo docker attach [容器名称/容器ID]
```
* 在已经启动的容器中执行命令
``` bash
sudo docker exec -it [容器名称/容器ID] /bin/bash
```
* 查看容器详细信息
``` bash
docker inspect [容器名称/容器ID]
```
* 查看容器资源信息
``` bash
sudo docker stats [容器名称/容器ID]
```
* 查看容器内进程
``` bash
sudo docker top [容器名称/容器ID]
```
* 查看日志
``` bash
sudo docker logs [容器名称/容器ID]
```
