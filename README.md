# 利用docker搭建的开发环境
docker开发环境，包括
. PHP
. MySQL
. Reids
. Nginx
. ZooKeeper
. Elasticsearch
. RabbitMQ

php包括拓展：math，memcache，xhprof性能分析

### 优势
1. 多版本PHP共存
2. 快速启动
3. 统一环境

### win7
windows7必须装虚拟机才能使用docker，开发环境建议关闭防火墙：systemctl stop firewalld.service 
1. 安装虚拟机
2. 暴露端口
3. 虚拟机挂载共享目录，如我这里是挂载的整个e盘：sudo mount -t vboxsf e /mnt/share/ 
4. 启动docker服务：systemctl start docker
5. 启动docker容器

### MacOS
1. 安装docker客户端
2. 启动docker容器


### 运行步骤
docker-composer up -d
- -d 以守护进程的方式运行