## 操作容器
# 新建并启动
* 命令：docker run [选项]
* 实例：`docker run ubuntu:14.04 /bin/echo 'Hello world'`

# 启动已终止容器
* 命令：docker start [选项]

# 守护态运行
* 通过添加-d参数来实现
* 实例：`docker run ubuntu:14.04 /bin/sh -c "while true; do echo hello world; sleep 1; done"`

# 查看输出结果
* docker logs

# 终止容器
* 使用 docker stop 来终止一个运行中的容器
* 终止状态的容器可以用 docker ps -a 命令看到

# 进入容器
* Docker自带命令：docker attach
* nsenter 工具在 util-linux 包2.23版本后包含

# 导出容器
* 格式：docker export [选项]
* 实例： `docker export 7691a814370e > ubuntu.tar`

# 导入容器
* 格式：docker import [选项]
* 实例：`docker import - test/ubuntu:v1.0`

# 删除容器
* 格式： docker rm [选项]
* 实例：`docker rm  trusting_newton` 删除一个处于终止状态的容器
* 实例：`docker rm $(docker ps -a -q` 清理所有处于终止状态的容器
