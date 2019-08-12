#########################镜像说明#########################
#继承自mysql 版本：5.7.22
#操作步骤：
#   下载mysql官方镜像： docker pull mysql:5.7.22
#   根据Dockerfile构建自己的镜像，主要是为了添加挂载信息 docker build -t mysql-img:v1 .
#   运行容器 docker run --name mysql-cont --network mynet --network-alias net.mysql -d -p 3306:3306 mysql-img:v1


#########################镜像说明#########################



# base images
FROM mysql:5.7.22

# auther
MAINTAINER cold

# port
EXPOSE 3306

# 挂载配置数据到宿主机,宿主机挂载路径自动生成,一般可在主机/var/lib/docker/volumes/ 中查找
VOLUME ["/etc/mysql/conf.d/","/var/lib/mysql/"]
