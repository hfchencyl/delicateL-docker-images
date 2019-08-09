#########################镜像说明#########################
#继承自jenkins 版本：2.60.3
#操作步骤：
#   下载jenkins官方镜像： docker pull jenkins:2.60.3
#   根据Dockerfile构建自己的镜像，主要是为了添加挂载信息 docker build -t jenkins-img:v1 .
#   运行容器 docker run --name jenkins-cont --network mynet --network-alias net.jenkins -d -p 8080:8080 jenkins-img:v1


#########################镜像说明#########################



# base images
FROM jenkins:2.60.3

# auther
MAINTAINER cold

# port
EXPOSE 8090

# 挂载配置数据到宿主机,宿主机挂载路径自动生成,一般可在主机/var/lib/docker/volumes/ 中查找
VOLUME ["/var/jenkins_home"]
