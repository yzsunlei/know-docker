# 使用镜像
## 拉取镜像
* 命令格式：docker pull [选项] [Docker Registry地址]<仓库名>:<标签>
* 实例：`docker pull ubuntu:14.04`

## 运行镜像
* 命令格式：docker run 各种选项
* 实例：`docker run -it --rm ubuntu:14.04 bash`  启动里面的bash并进行交互式操作
 
## 列出镜像
* 命令格式：docker images
* 可以查看到仓库名、标签、镜像id、创建时间、占用空间

## 提交新的镜像
* 命令格式：docker commit [选项] <容器ID或容器名> [<仓库名>[:<标签>]]
* 实例：`docker commit --author "Zhang" --message "修改了默认网页" webserver nginx:v2`

## 查看镜像历史记录
* 命令格式：docker history [选项]
* 实例：`docker history nginx:v2`

## 导入镜像
* 命令格式：docker import [选项] <文件>|<URL>|- [<仓库名>[:<标签>]]
* 实例：`docker import http://download.openvz.org/template/precreated/ubuntu-14.04-x86_64-minimal.tar.gz openvz/ubuntu:14.04`

## 保存镜像
* 命令格式：docker save <镜像名> [选项]
* 实例：`docker save alpine | gzip > alpine-latest.tar.gz`

## 加载镜像
* 命令格式： docker load [选项]
* 实例：`docker load -i alpine-latest.tar.gz`

## 删除镜像
* 命令格式：docker rmi [选项] <镜像1> [<镜像2> ...]
* 实例：`docker rmi centos`
