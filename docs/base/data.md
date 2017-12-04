# 数据管理
## 创建数据卷
* 格式：docker run [选项]
* 实例：`docker run -d -P --name web -v /webapp training/webapp python app.py`

## 删除数据卷
* 使用 docker rm -v 这个命令

## 查看数据卷的具体信息
* 实例：`docker inspect web`

## 创建数据卷容器
* 实例：`docker run -d -v /dbdata --name dbdata training/postgres echo Data-only container for postgres`

## 备份数据
* 实例：`docker run --volumes-from dbdata -v $(pwd):/backup ubuntu tar cvf /backup/backup.tar /dbdata`

## 恢复数据
* 实例：`docker run -v /dbdata --name dbdata2 ubuntu /bin/bash`