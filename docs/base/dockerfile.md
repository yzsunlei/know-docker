## Dockerfile指令
# COPY 复制文件
* 格式：COPY <源路径>... <目标路径>
* 实例：`COPY package.json /usr/src/app/`

# ADD 更高级的复制文件
* 试图去下载这个链接的文件放到目标路径中
* 实例：ADD ubuntu-xenial-core-cloudimg-amd64-root.tar.gz /

# CMD 容器启动命令
* shell 格式：CMD <命令>
* exec 格式：CMD ["可执行文件", "参数1", "参数2"...]
* 实例：`CMD echo $HOME`

# ENTRYPOINT 入口点
* 实例：`CMD [ "curl", "-s", "http://ip.cn" ]`

# ENV 设置环境变量
* 格式：ENV <key1>=<value1> <key2>=<value2>...
* 实例：`ENV NODE_VERSION 7.2.0`

# ARG 构建参数
* 格式：ARG <参数名>[=<默认值>]
* 实例：

# VOLUME 定义匿名卷
* 格式：VOLUME <路径>
* 实例： `VOLUME /data`

# EXPOSE 暴露端口
* 格式：EXPOSE <端口1> [<端口2>...]
* 实例：`EXPOSE 8080`

# WORKDIR 指定工作目录
* 格式： WORKDIR <工作目录路径>
* 实例：`WORKDIR /app`

# USER 指定当前用户
* 格式：USER <用户名>
* 实例：`USER redis`

# HEALTHCHECK 健康检查
* 格式：HEALTHCHECK [选项] CMD <命令>
* 实例：`HEALTHCHECK --interval=5s --timeout=3s` 每5s检查一次，超过3s没响应就视为失败

# ONBUILD 为他人做嫁衣裳
* 格式：ONBUILD <其它指令>
* 实例：`ONBUILD RUN [ "npm", "install" ]`