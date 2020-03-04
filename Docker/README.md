docker run  下载 创建  运行
--name  指定名称
--rm  停止后删除 
-p  外部端口:内部端口   
docker stop
docker pull 下载 
docker create 创建
docker start 启动

查看日志 
docker log myNgix

docker inspect myNgix 查看容器的所有信息

容器其实是一个精简版的操作系统  可以进入
docker exec -it myNginx bash

docker ps 容器列表
docker images 镜像列表

镜像文件 Dockfile
docker build -t image_name(镜像名称) ./(镜像文件路径)
分配容器
 docker run -p 80:80 image_name
 
 
 docker ps -s  查看大小
 
 docker history myNgnix 查看镜像分层



