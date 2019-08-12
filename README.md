# delicateL-docker-images
delicateL-docker-images

 说明： 本工程维护基础docker镜像
 
 一、容器依赖顺序：
    容器启动必须按照顺序，否则nginx连接不到其他网络会报错
 
      nginx依赖了jenkins、应用服务delicate，所有nginx要最后启动
 
 二、各个容器细节
    1、nginx: 在部署jenkins的时候，理论上来说业务应用和jenkins要区分开，但是公用一台服务器的话，想出来一个方案，就是为jenkins单独配置nginx监听；需要阿里云主机上开放18880端口；
               nginx配置过程中，主要要消除default.conf的影响
               
 三、网络： 
       创建docker网络（容器之间在这个网络内部通讯）： docker network create mynet
   
   
   
   
 额外参考资料：
 1、容器网络连接，推荐方法三： https://blog.csdn.net/subfate/article/details/81396532