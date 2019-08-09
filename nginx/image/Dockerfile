#########################镜像说明#########################
#继承自nginx 版本：1.17.2
#操作步骤：
#   下载nginx官方镜像： docker pull nginx:1.17.2
#   根据当前路径的Dockerfile构建自己的镜像，主要是为了添加挂载信息: docker build -t nginx-img:v1 .
#   运行容器： docker run --name nginx-cont --link jenkins-cont:jenkins-cont -d -p 80:80 nginx-img:v1

#########################镜像说明#########################


# base images
FROM nginx:1.17.2

# auther
MAINTAINER cold

# add file to image
ADD ./conf/nginx-jenkins.conf /etc/nginx/conf.d/nginx-jenkins.conf

#ADD ./conf /my/conf
#ADD ./scripts /my/scripts
# 测试过这样直接加可行
#ADD ./html/index.html /usr/share/nginx/html/index.html


# 运行脚本，RUN是build的时候就会运行
#RUN chmod 755 /my/scripts/run.sh

# port
EXPOSE 80

# 挂载配置数据到宿主机,宿主机挂载路径自动生成,一般可在主机/var/lib/docker/volumes/ 中查找
VOLUME ["/etc/nginx/","/var/log/nginx/"]
