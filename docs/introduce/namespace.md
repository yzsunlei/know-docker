# 命名空间（此节可以先跳过）
## 主机UTS
* hostname隔离

## 进程PID
* 处理pid
* 要激活PID namespace，只需要把“CLONE_NEWPID”标记添加到clone的调用中

## 网络NET
* 隔离网络接口

## 消息IPC
* 进程间通讯
* 要激活IPC namespace，只需要把“CLONE_NEWPIC”标记添加到clone的调用中

## 文件系统MNT

## 挂载点NS
* 隔离挂载表
* 要激活NS namespace，只需要把“CLONE_NEWNS”标记添加到clone的调用中

