# 快速安装
## ubuntu14.04安装
* `apt-get update` 更新ubuntu软件包缓存
* `apt-get install apt-transport-https ca-certificates curl software-prpperties-common` 添加使用HTTPS传输的软件包以及CA证书
* `curl -fsSL https://mirrors.ustc.edu.cn/docker-ce/linux/ubuntu/gpg | sudo apt-key add -` 添加软件源的GPG密钥
* `add-apt-repository deb [arch=amd64] https://mirrors.ustc.edu.cn/docker-ce/linux/ubuntu $(lsb_release -cs) stable"` 添加稳定版本的Docker CE APT镜像源
* `apt-get install docker-ce` 命令安装docker-ce
* `service docker start` 启动docker
* `groupadd docker` 建立docker用户组
* `usermod -aG docker $USER` 将当前用户加入docker用户组

## win10安装
* [点击链接下载Docker Ce](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe)
* 双击运行，然后下一步下一步，简单的没话说