---

layout: post
title:  Docker构建Python(小知识)
categories: [开发工具,Docker]
tags:  Docker
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924061557321.png
---

# Docker构建Python(小知识)

> 创建Python容器

- 创建Python容器

``` shell
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker pull python
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker run -it -d --name=p1 -p 9500:5000 -v /docker_/project/:/root/project --net mynet --ip 172.18.0.2 python:3.8 bash
15466f0fe05ff8e2ed104edf66965c257f43a9570b48864460cd3dcd81721eb6

```

- 为pip命令加速

  为了加快pip命令下载安装扩展程序的速度,可以使用国内服务来提速

  比如连接清华大学的服务器下载扩展程序,只需要在pip命令结尾加上特定的参数

  ```shell
  pip install flask -i https://pypi.tuna.tsinghua.edu.cn/simple
  ```

  ![image-20200924061557321](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924061557321.png)

> 创建MySQL容器

- 下载MySQL镜像

用docker pull 命令下载8.0.18版本的MySQL镜像

``` shell
docker pull mysql:8.0.18 #下载特定版本的镜像文件 
docker pull mysql		 #下载最新版本的镜像文件
```

- 创建MySQL容器

用docker run 命令创建MySQL容器,并且做好端口映射和目录挂载

```shell
docker run --name m1 -p 4306:3306 --net mynet --ip 172.18.0.3 -v /docker_/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql:8.0.18
```

- 创建数据表,写入记录

安装Navicat软件

MySQL客户端有很多优秀的客户端软件,但是其中最为优秀的是Navicat

https://www.navicat.com.cn/download/navicat-premium

![image-20200923220900084](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200923220900084.png)





​	