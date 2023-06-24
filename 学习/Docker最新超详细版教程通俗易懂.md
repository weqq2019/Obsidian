---
layout: post
title:  Docker最新超详细版教程通俗易懂
categories: [开发工具,Docker]
tags:  Docker
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921162402469.png
---



![image-20200923191545121](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200923191545121.png)

# Docker概述

## Docker为什么出现？

一款产品:开发--上线 两套环境！应用环境,应用配置！

开发    ----    运维.    问题:我在我的电脑上可以运行！版本更新,导致服务不可用！对于运维来说,考验就十分大？

环境配置是十分的麻烦,每一个机器都要部署环境(集群Redis、ES、Hadoop......)!费时费力.

发布一个项目(jar+(Redis Mysql jdk ES)),项目能不能都带上环境安装打包！

之前在服务器配置一个应用的环境 Redis MySQL jdk ES Hadoop,配置超麻烦了,不能够跨平台.

windows,最后发布到Linux!

传统:开发jar,运维来做！

现在:开发打包部署上线,一套流程做完！



java -- apk -- 发布 (应用商店) ---- 张三使用apk ---- 安装即可用！

java -- jar (环境)  ---- 打包项目带上环境(镜像) ---- (Docker仓库:商店) ---- 直接运行即可！



Docker给以上的问题,提出了解决方案！

Docker的思想就来自于集装箱！

JRE ----  多个应用 (端口冲突) ---- 原来都是交叉的！

隔离:Docker核心思想！打包装箱！每个箱子是互相隔离的.

水果  生化武器

Docker 通过隔离机制,可以将服务器用到极致！



本质:所有的技术都是因为出现了一些问题,我们需要去解决,才去学习！



## Docker的历史

2010年,几个搞IT的年轻人,就在美国成立了一家公司`dotCloud`

做一些 pass 的云计算服务！LXC 有关的容器技术！

他们将自己的技术 (容器化技术) 命名 就是Docker!

Docker 刚刚诞生的时候,没有引起行业的注意！`dotCloud`,就活不下去！

` 开源 `

开发源代码！

2013年,Docker开源！

Docker越来越多的人发现了Docker的优点！火了,Docker每个月都会更新一个版本！

2014年4月9日,Docker1.0发布！

Docker为什么这么火？

在容器技术出来之前,我们都是使用虚拟机技术！

虚拟机:在windows中装一个Vmware , 通过这个软件我们可以虚拟出来一台或者多台电脑！笨重！

虚拟机也是属于虚拟化技术,Docker容器技术,也是一种虚拟化技术！

``` shell
vm: linux centos原生镜像(一个电脑) 隔离,需要开启多个虚拟机！几个G   几分钟
docker:隔离, 镜像 (最核心的环境 4M + jdk + mysql) 十分的小巧,运行镜像就可以了！小巧！ 几个M KB 秒级启动！
```

到现在,所有开发人员都必须要会Docker!

> 聊聊Docker

Docker是基于 Go 语言开发的！开源项目！

 官网:https://www.docker.com/

![image-20200921172558069](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921172558069.png)

文档地址:https://docs.docker.com/  Docker的文档是超级详细的！

仓库地址:https://hub.docker.com/

 ## Docker能干嘛

> 之前的虚拟机技术！

![image-20200921174312086](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921174312086.png)

虚拟机技术缺点:

1、资源占用十分多

2、冗余步骤多

3、启动很慢！



> 容器化技术

==容器化技术不是模拟的一个完整的操作系统==

![image-20200921174947089](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921174947089.png)

比较Docker 和虚拟机技术的不同:

- 传统虚拟机,虚拟出一条硬件,运行一个完整的操作系统,然后在这个系统上安装和运行软件
- 容器内的应用直接运行在宿主机的内容,容器是没有自己的内核的,也没有虚拟我们的硬件,所以就轻便了
- 每个容器间是互相隔离,每个容器内都有一个属于自己的文件系统,互不影响.

> DevOps(开发,运维)

**应用更快速的交付和部署**

传统:一堆帮助文档,安装程序

Docker:打包镜像发布测试,一键运行

**更便捷的升级和扩缩容**

使用了Docker之后,我们部署应用和塔积木一样！

项目打包为一个镜像,扩展 服务器A！服务器B

**更简单的系统运维**

在容器化之后,我们的开发,测试环境都是高度一致的.

**更高效的计算资源利用**

Docker是内核级别的虚拟化,可以再一个物理机上可以运行很多的容器实例！服务器的性能可以被压榨到极致.

只要学不死,就往死里学！

# Docker 安装

## Docker的基本组成

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921181126286.png)

**镜像(image):**

Docker镜像就好比是一个模板,可以通过这个模板来创建容器服务,tomcat镜像 ===>run ===>tomcat01(提供服务器),

通过这个镜像可以创建多个容器(最终服务运行或者项目运行就是容器中的.)

**容器(container):**

Docker利用容器技术,独立运行一个或者一个组应用,通过镜像来创建的.

启动,停止,删除,基本命令！

目前就可以把这个容器理解为就是一个简易的linux系统

**仓库(repository):**

仓库就是存放镜像的地方！

仓库分为公有仓库和私有仓库！

Docker Hub(默认是国外的)

阿里云....都有容器服务器(配置镜像加速！)

## 安装 Docker

> 环境准备

1.需要会一点点的linux基础

2.CentOS7

3.我们使用Xshell连接远程服务器进行操作！

> 环境查看

``` shell
# 系统内核是 3.10 以上的
[root@iZm5egx0inbsssu7xq22z7Z ~]# uname -r
4.18.0-193.14.2.el8_2.x86_64
```

``` shell
# 系统版本
[root@iZm5egx0inbsssu7xq22z7Z ~]# cat /etc/os-release 
NAME="CentOS Linux"
VERSION="8 (Core)"
ID="centos"
ID_LIKE="rhel fedora"
VERSION_ID="8"
PLATFORM_ID="platform:el8"
PRETTY_NAME="CentOS Linux 8 (Core)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:centos:centos:8"
HOME_URL="https://www.centos.org/"
BUG_REPORT_URL="https://bugs.centos.org/"

CENTOS_MANTISBT_PROJECT="CentOS-8"
CENTOS_MANTISBT_PROJECT_VERSION="8"
REDHAT_SUPPORT_PRODUCT="centos"
REDHAT_SUPPORT_PRODUCT_VERSION="8"
```

> 安装

帮助文档:

### 1、卸载旧版本

较旧的Docker版本称为`docker`或`docker-engine`。如果已安装这些程序，请卸载它们以及相关的依赖项。

```shell
sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
```

### 2、需要的安装包

``` shell
sudo yum install -y yum-utils
```

### 3、设置镜像的仓库

``` shell
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo #默认是从国外的！
    
sudo yum-config-manager \
	--add-repo \
	http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo #推荐使用阿里云的,十分的快
```

### 更新yum软件索引

``` shell
yum makecache fast #Centos7

yum makecache #centos8没有该参数，解决办法为：去掉fast参数，就可以了

```



### 4、安装docker相关的依赖 docker-ce 社区  ee企业版

```shell
sudo yum install docker-ce docker-ce-cli containerd.io #Centos7
```

**Centos8**

 **1、错误内容**

```
package docker-ce-3:19.03.2-3.el7.x86_64 requires containerd.io >= 1.2.2-3, but none of the providers can be installed
- cannot install the best candidate for the job
- package containerd.io-1.2.2-3.3.el7.x86_64 is excluded
- package containerd.io-1.2.2-3.el7.x86_64 is excluded
- package containerd.io-1.2.4-3.1.el7.x86_64 is excluded
- package containerd.io-1.2.5-3.1.el7.x86_64 is excluded
- package containerd.io-1.2.6-3.3.el7.x86_64 is excluded
(try to add '--skip-broken' to skip uninstallable packages or '--nobest' to use not only best candidate packages)
12345678
```

2、分析原因

看上面的内容，说的是containerd.io >= 1.2.2-3 ，意思就是 containerd.io 的版本必须大于等于 1.2.2-3

3、解决

1、要么就降低docker 的版本

2、如果不想降低docker 版本，那么就更新 containerd.io 的版本

```shell
wget https://download.docker.com/linux/centos/7/x86_64/edge/Packages/containerd.io-1.2.6-3.3.el7.x86_64.rpm
yum install -y  containerd.io-1.2.6-3.3.el7.x86_64.rpm
```

然后重新安装最新版本的docker 即可成功安装

``` shell
sudo yum install docker-ce docker-ce-cli containerd.io
```



 4、检查是否安装成功

```
docker -v
```

### 5、启动docker

``` shell
systemctl start docker
```

6、使用docker version 是否安装成功！

![image-20200921190010693](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921190010693.png)

### 7、hello-world

``` shell
docker run hello-world
```



![image-20200921190244097](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921190244097.png)

### 8、查看一下下载的这个 hello-world 镜像

``` shell
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              bf756fb1ae65        8 months ago        13.3kB

```

了解:卸载docker

```shell
#1、卸载依赖
sudo yum remove docker-ce docker-ce-cli containerd.io
#2、删除资源
sudo rm -rf /var/lib/docker

# /var/lib/docker docker的默认工作路径！
```

## 阿里云镜加速

1、登录阿里云找到容器服务

![image-20200921191245127](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921191245127.png)

2、找到镜像加速地址

![image-20200921191520314](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921191520314.png)

``` shell
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://vevt86ru.mirror.aliyuncs.com"]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
```

> 回顾HelloWorld流程

![image-20200921190244097](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921190244097.png)

![image-20200921192404010](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921192404010.png)

## 底层原理

Docker是什么工作的？

Docker 是一个 Client -Server结构的系统,Docker的守护进程运行的主机上.通过Socket从客户端访问！

DockerServer接收到Docker-Client的指令,就会执行这个命令！

![image-20200921193319537](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921193319537.png)

Docker为什么比VM快

1、Docker有着比虚拟机更少的抽象层、

2、Docker 利用的是宿主机的内核, VM 需要是Guest OS.

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921193934961.png)

所以说,新建一个容器的时候,Docker不需要像虚拟机一样重新加载一个操作系统内核,避免引导,虚拟机是加载Guset OS,分钟级别的,而docker 是利用 宿主机的操作系统吗,省略了这个复杂的过程,秒级！

![image-20200921194306545](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921194306545.png)



之后学习完毕所有命令,再回过来头看这段理论,就会很清晰！

#  Docker的常用命令

![image-20200923202515510](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200923202515510.png)

## 帮助命令

``` shell
docker version			#显示docker的版本信息
docker info				#显示docker的系统信息,包括镜像和容器的数量
docker 命令 --help	   #帮助命令
```

帮助命令地址:https://docs.docker.com/engine/reference/commandline

## 镜像命令

**docker images**

``` shell
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              bf756fb1ae65        8 months ago        13.3kB

# 解释
REPOSITORY	    镜像的仓库源
TAG				镜像的标签	
IMAGE ID		镜像的ID
CREATED			镜像的创建时间
SIZE			镜像的大小

# 可选项
-a, --all		#列出所有镜像
-q,--quiet		#只显示镜像的id
```

**docker search 搜索镜像**

``` shell
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker search mysql
NAME                              DESCRIPTION                                     STARS               OFFICIAL            AUTOMATED
mysql                             MySQL is a widely used, open-source relation…   9976                [OK]                
mariadb                           MariaDB is a community-developed fork of MyS…   3652                [OK]                
mysql/mysql-server                Optimized MySQL Server Docker images. Create…   728  


# 可选项,通过搜索来过滤
-- filter=STARS=3000		#搜索出来的镜像就是START大于3000的
```

**docker pull** 下载镜像

``` shell
#下载镜像 docker pull 镜像名:[:tag]
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker pull mysql
Using default tag: latest	# 如果不写 tag.默认就是latest
latest: Pulling from library/mysql # 分层下载:docker image的核心 联合文件系统
d121f8d1c412: Pull complete 
f3cebc0b4691: Pull complete 
1862755a0b37: Pull complete 
489b44f3dbb4: Pull complete 
690874f836db: Pull complete 
baa8be383ffb: Pull complete 
55356608b4ac: Pull complete 
dd35ceccb6eb: Pull complete 
429b35712b19: Pull complete 
162d8291095c: Pull complete 
5e500ef7181b: Pull complete 
af7528e958b6: Pull complete 
Digest: sha256:e1bfe11693ed2052cb3b4e5fa356c65381129e87e38551c6cd6ec532ebe0e808 # 签名
Status: Downloaded newer image for mysql:latest 
docker.io/library/mysql:latest # 真实地址

#等价于它
docker pull mysql
docker pull docker.io/library/mysql:latest

# 指定下载
docker pull mysql:5.7
```

![image-20200921201238590](C:%5CUsers%5CAlienware%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20200921201238590.png)

**docker rmi** 删除镜像！

```shell
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker rmi -f 容器ID		#删除指定的容器
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker rmi -f 容器ID 容器ID 容器ID 容器ID #删除多个容器
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker rmi -f $(docker images -aq) #删除全部的容器
```

## 容器命令

说明:我们有了镜像才可以创建容器,linux,下载一个centos镜像来测试学习

``` shell
docker pull centos
```

新建容器并启动

```shell
docker run [可选参数] image

#参数说明
--name="name"	容器名字	tomcat01 tomcat02,用来分容器
-d				后台方式运行	
-it				使用交互方式运行,进入容器查看内容
-p				指定容器的端口	-p	8080:8080
	-p	主机端口:容器端口
	-p	容器端口
	容器端口
-P				随机指定端口

#测试	启动并进入容器
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker run -it centos /bin/bash
[root@f99434b9e184 /]#	ls #查看容器内的centos ,基础版本, 很多命令都是不完善的！
bin  dev  etc  home  lib  lib64  lost+found  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

```

**列出所有的运行容器

```shell
#docker ps 命令
	#列出当前正在运行的容器
-a	#列出当前正在运行的容器+带出历史运行过的容器
-n=?#显示最近创建的容器
-q	#只显示容器的编号
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                     PORTS               NAMES
f99434b9e184        centos              "/bin/bash"         5 minutes ago       Exited (0) 3 minutes ago                       nervous_jones
632ac08035ce        bf756fb1ae65        "/hello"            2 hours ago         Exited (0) 2 hours ago                         flamboyant_meninsky
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker ps -n=1
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                     PORTS               NAMES
f99434b9e184        centos              "/bin/bash"         9 minutes ago       Exited (0) 6 minutes ago                       nervous_jones
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker ps -q
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker ps -aq
f99434b9e184
632ac08035ce
```

退出容器

```shell
exit	#直接容器停止并退出
ctrl+p+q	#容不停止退出
```

删除容器

``` shell
docker rm 容器id					#删除指定的容器 不能删除正在运行的容器,强制删除 rm -f
docker rm -f $(dock ps -aq)		 #删除全部的容器
docker ps -a -q | xargs docker rm #删除所有的容器
```

启动和停止容器的操作

```shell
docker start 容器id		#启动容器
docker restart 容器id		#重启容器
docker stop    容器id		#停止当前正在运行的容器
docker kill    容器id		#强制停止当前容器
```

## 常用其他命令

后台启动容器

```shell
# 命令 docker run -d 镜像名！
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker run -d centos

#问题docker ps 发现centos 停止了

#常见的坑,docker 容器使用后台运行,就必须要有要一个前台进程,docker发现没有应用,就会自动停止
#nginx.容器启动后,发现自己没有提供服务,就会立刻停止,就是没有程序了
```

查看日志

```shell
docker logs -f -t  容器id,没有日志

# 自己编写一段shell脚本
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker run -d centos /bin/sh -c "while true; do echo iZm5egx0inbsssu7xq22z7Z docker_;sleep 1;done"
3253f72007417933e56494e987513c69a94b3e52c794749f1cc000cce6dd787c
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
3253f7200741        centos              "/bin/sh -c 'while t…"   4 seconds ago       Up 3 seconds                            happy_nightingale

显示日志
-tf #显示日志
--tail	#要显示日志条数
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker logs -ft --tail 10 3253f7200741

```

查看容器进程信息 ps

```shell
#命令 docker top 容器id

[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker top 3253f7200741
UID                 PID                 PPID                C                   STIME     
root                17326               17310               0                   21:07     
root                17841               17326               0                   21:13     
```

查看镜像的元数据

```shell
#命令
docker inspect 容器id

#测试

[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker inspect 3253f7200741
[
    {
        "Id": "3253f72007417933e56494e987513c69a94b3e52c794749f1cc000cce6dd787c",
        "Created": "2020-09-21T13:07:11.577126979Z",
        "Path": "/bin/sh",
        "Args": [
            "-c",
            "while true; do echo iZm5egx0inbsssu7xq22z7Z docker_;sleep 1;done"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 17326,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2020-09-21T13:07:12.114310101Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:0d120b6ccaa8c5e149176798b3501d4dd1885f961922497cd0abef155c869566",
        "ResolvConfPath": "/var/lib/docker/containers/3253f72007417933e56494e987513c69a94b3e52c794749f1cc000cce6dd787c/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/3253f72007417933e56494e987513c69a94b3e52c794749f1cc000cce6dd787c/hostname",
        "HostsPath": "/var/lib/docker/containers/3253f72007417933e56494e987513c69a94b3e52c794749f1cc000cce6dd787c/hosts",
        "LogPath": "/var/lib/docker/containers/3253f72007417933e56494e987513c69a94b3e52c794749f1cc000cce6dd787c/3253f72007417933e56494e987513c69a94b3e52c794749f1cc000cce6dd787c-json.log",
        "Name": "/happy_nightingale",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "default",
            "PortBindings": {},
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Capabilities": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "KernelMemory": 0,
            "KernelMemoryTCP": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/fe47b326ca3f0b10ce49c6de7460fcd5a480c997c49538203e2f273f26740261-init/diff:/var/lib/docker/overlay2/69da5c6bed605fc9a0bf0624a6290de42cda24892caa8618e04317dbcdeb7caf/diff",
                "MergedDir": "/var/lib/docker/overlay2/fe47b326ca3f0b10ce49c6de7460fcd5a480c997c49538203e2f273f26740261/merged",
                "UpperDir": "/var/lib/docker/overlay2/fe47b326ca3f0b10ce49c6de7460fcd5a480c997c49538203e2f273f26740261/diff",
                "WorkDir": "/var/lib/docker/overlay2/fe47b326ca3f0b10ce49c6de7460fcd5a480c997c49538203e2f273f26740261/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "3253f7200741",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/bin/sh",
                "-c",
                "while true; do echo iZm5egx0inbsssu7xq22z7Z docker_;sleep 1;done"
            ],
            "Image": "centos",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "org.label-schema.build-date": "20200809",
                "org.label-schema.license": "GPLv2",
                "org.label-schema.name": "CentOS Base Image",
                "org.label-schema.schema-version": "1.0",
                "org.label-schema.vendor": "CentOS"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "bc5328bd9a3b014479fe5df124071c19959faf490339f33e11ce1fd3322b2a64",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {},
            "SandboxKey": "/var/run/docker/netns/bc5328bd9a3b",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "f4c7a56b6d7f3a3c6f77b6abb60ccf7532e802b63a9d45d1eb871e9fdf548501",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "02:42:ac:11:00:02",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "695eac0241fefde0ef723c12b2bb6a74081216f9738bb5a1b85d9543825d44b2",
                    "EndpointID": "f4c7a56b6d7f3a3c6f77b6abb60ccf7532e802b63a9d45d1eb871e9fdf548501",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:11:00:02",
                    "DriverOpts": null
                }
            }
        }
    }
]

```

进入当前正在运行的容器

```shell
# 我们通常容器都是使用台式方式运行的,需要进入容器,修改一些配置

#命令
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
3253f7200741        centos              "/bin/sh -c 'while t…"   12 minutes ago      Up 12 minutes                           happy_nightingale
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker exec -it 3253f7200741 /bin/bash
[root@3253f7200741 /]# ls
bin  dev  etc  home  lib  lib64  lost+found  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
[root@3253f7200741 /]# ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 13:07 ?        00:00:00 /bin/sh -c while true; do echo iZm5egx0inbsssu7xq22z7Z docker_;sleep 1;done
root         802       0  1 13:20 pts/0    00:00:00 /bin/bash
root         826       1  0 13:20 ?        00:00:00 /usr/bin/coreutils --coreutils-prog-shebang=sleep /usr/bin/sleep 1
root         827     802  0 13:20 pts/0    00:00:00 ps -ef

#方式二
#命令
docker attach 容器id
#测试
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker attach 3253f7200741
正在执行当前的代码...

#docker exec #进入容器后开启一个新的终端,可以在里面操作(常用)
#docker attach#进入容器正在执行的终端,不会启动新的进程！
```

从容器内拷贝文件到主机上

```shell
docker cp 容器id:容器内路径 目的的主机路径

[root@iZm5egx0inbsssu7xq22z7Z ~]# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS              PORTS               NAMES
c47cf332e12c        centos              "/bin/bash"         About a minute ago   Up About a minute                       upbeat_mendeleev
[root@iZm5egx0inbsssu7xq22z7Z ~]# cd /home
#查看当前主机目录下
[root@iZm5egx0inbsssu7xq22z7Z home]# ls
er  git  hexo
[root@iZm5egx0inbsssu7xq22z7Z home]# touch weqq.java
[root@iZm5egx0inbsssu7xq22z7Z home]# ls
er  git  hexo  weqq.java
[root@iZm5egx0inbsssu7xq22z7Z home]# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS              PORTS               NAMES
c47cf332e12c        centos              "/bin/bash"         About a minute ago   Up About a minute                       upbeat_mendeleev
#进入docker容器内容
[root@iZm5egx0inbsssu7xq22z7Z home]# docker attach c47cf332e12c
[root@c47cf332e12c /]# cd /home
[root@c47cf332e12c home]# ls
#在容器内新建一个文件
[root@c47cf332e12c home]# touch test.java
[root@c47cf332e12c home]# ls
test.java
[root@c47cf332e12c home]# exit
exit
[root@iZm5egx0inbsssu7xq22z7Z home]# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
[root@iZm5egx0inbsssu7xq22z7Z home]# docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
c47cf332e12c        centos              "/bin/bash"         3 minutes ago       Exited (0) 10 seconds ago                       upbeat_mendeleev
#将这文件拷贝出来到主机上
[root@iZm5egx0inbsssu7xq22z7Z home]# docker cp c47cf332e12c :/home/test.java /home
"docker cp" requires exactly 2 arguments.
See 'docker cp --help'.

Usage:  docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH|-
	docker cp [OPTIONS] SRC_PATH|- CONTAINER:DEST_PATH

Copy files/folders between a container and the local filesystem
[root@iZm5egx0inbsssu7xq22z7Z home]# docker cp c47cf332e12c:/home/test.java /home
[root@iZm5egx0inbsssu7xq22z7Z home]# ls
er  git  hexo  test.java  weqq.java

#拷贝是一个手动过程,未来我们使用 -v卷的技术,可以实现

```

学习方式:将我的所有命令全部敲一遍,自己记录笔记！

小结

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921214005357.png)

```shell
docker attach	# 当前 shell 下 attach 连接指定运行镜像
docker build	# 通过 Dockerfile 定制镜像
docker commit	# 提交当前容器为新的镜像
docker cp		# 从容器中拷贝指定文件或者目录到宿主机中
docker create	#创建一个新的容器,同 run ,但不启动容器
docker diff		#查看 docker 容器变化
docker events	#从 docker 服务获取容器实时事件
docker exec		#在已存在的容器上运行命令
docker export	#导出容器的内容流作为一个 tar 归档文件 [对应 import]
docker history	#展示一个镜像形成历史
docker image	#列出系统当前镜像
docker import	#从 tar 包中的内容创建一个新的文件系统映像[对应 export]
docker info		#显示系统相关信息
docker inspect	#查看容器详细信息
docker kill	 	#kill 指定 docker 容器
docker load	 	#从一个 tar 包中加载一个镜像[对应 save]
docker login	#注册或者登录一个 docker 源服务器
docker logout	#从当前 Docker registry 退出
docker logs		#输出当前容器日志消息
docker port		#查看映射端口对应的容器内部源端口
docker pause    #暂停容器
docker ps		#列出容器列表
docker pull	  	#从docker镜像源服务器拉取指定镜像或库镜像
docker restart	#重启运行的容器
docker rm		#移除一个或者多个容器
docker rmi		#移除一个或多个镜像[无容器使用该镜像才可删除,否则需删除相关容器才可继续或 -f 强制删除]
docker run		#创建一个新的容器并运行一个命令
docker save		#保存一个镜像为一个 tar 包[对应 load]
docker search	#在 docker hub 中 搜索镜像
docker start	#启动容器
docker stop		#停止容器
docker tag		#给源中镜像打标签
docker top		#查看容器中运行的进程信息
docker unpause	#取消暂停容器
docker version	#查看 docker 版本号 
docker wait		#截取容器停止时的退出状态值
```

docker的命令是十分多的,上面我们学习的那些都是最常用的容器和镜像的命令,之后我们还会学习很多

接下来就是一堆的练习

作业练习

Docker 安装Nginx

```shell
#1、搜索镜像 search 建议大家去docker搜索 ,可以看到帮助文档
#2、下载镜像 pull
#3、运行测试
# docker images
[root@iZm5egx0inbsssu7xq22z7Z home]# docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
d121f8d1c412: Pull complete 
ebd81fc8c071: Pull complete 
655316c160af: Pull complete 
d15953c0e0f8: Pull complete 
2ee525c5c3cc: Pull complete 
Digest: sha256:c628b67d21744fce822d22fdcc0389f6bd763daac23a6b77147d0712ea7102d0
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest
[root@iZm5egx0inbsssu7xq22z7Z home]# docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
nginx               latest              7e4d58f0e5f3        11 days ago         133MB
centos              latest              0d120b6ccaa8        5 weeks ago         215MB
[root@iZm5egx0inbsssu7xq22z7Z home]# docker run -d --name nginx01 -p 3344:80 nginx
#-d 后台运行
#--name 给容器命名
#-p 宿主机端口,容器
15b30e1bdadfa4e5c7026e22409c16c4b570f737da49fc290204bcd33348cc64
[root@iZm5egx0inbsssu7xq22z7Z home]# docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                  NAMES
15b30e1bdadf        nginx               "/docker-entrypoint.…"   9 seconds ago       Up 7 seconds        0.0.0.0:3344->80/tcp   nginx01
[root@iZm5egx0inbsssu7xq22z7Z home]# curl localhost:3344
#进入容器
[root@iZm5egx0inbsssu7xq22z7Z home]# docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                  NAMES
15b30e1bdadf        nginx               "/docker-entrypoint.…"   27 minutes ago      Up 27 minutes       0.0.0.0:3344->80/tcp   nginx01
[root@iZm5egx0inbsssu7xq22z7Z home]# docker exec -it nginx01 /bin/bash
root@15b30e1bdadf:/# ls
bin  boot  dev	docker-entrypoint.d  docker-entrypoint.sh  etc	home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@15b30e1bdadf:/# cd etc/nginx/
root@15b30e1bdadf:/etc/nginx# ls
conf.d	fastcgi_params	koi-utf  koi-win  mime.types  modules  nginx.conf  scgi_params	uwsgi_params  win-utf


```

![image-20200921224752431](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921224752431.png)

思考问题:我们再次发动nginx配置文件,都需要进入容器？十分的麻烦,我要是可以在容器外部提供一个映射路径,达到在容器修改文件名,容器内部就可以自动修改？

> 作业:docker来装一个tomcat

```shell
# 官方的使用
docker run -it --rm tomcat:9.0

# 我们之前的启动都是后台,停止了容器之后,容器还是可以查看  docker run -it --rm 一般用来测试,用完删除

# 下载在启动
docker pull tomcat

# 启动运行
docker run -d -p 3355:8080 --name tomcat1 tomcat

#测试访问没有问题

#进入容器
[root@iZm5egx0inbsssu7xq22z7Z home]# docker exec -it tomcat1 /bin/bash

#发现问题:1、linux命令少了,2、没有webapps.阿里云镜像的原因.默认是最小的镜像,所有不必要的都剔除掉.
#保证最小可运行的环境！
```

![image-20200921232634580](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200921232634580.png)



思考问题:我们以后要部署项目,如果每次都需要进入容器？十分的麻烦,我要是可以在容器外部提供一个映射路径,webapps,我们在外部放置项目,就自动同步的内部就好了！

> 作业:部署 es + kibrana

```shell
# es 暴露的端口很多！
# es 十分的耗内存
# es 的数据一般需要放置到安全目录！挂载
# -- net somenetwork ? 网络配置

# 启动elasticsearch
$ docker run -d --name elasticsearch  -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:7.6.2

# 启动了 linux就卡住了 docker stats 查看 CPU 的状态

# es 是十分耗内存的, 1.xG.  1核2G!

# 赶紧关闭,增加内存的限制

# 赶紧关闭,增加内存的限制,修改配置文件 -e 环境配置修改
$ docker run -d --name elasticsearch -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" -e ES_JAVA_OPTS="-Xms64m -Xmx512m" elasticsearch:7.6.2

```

![image-20200922001526721](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922001526721.png)

![image-20200922001833149](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922001833149.png)

作业:使用kibana连接es?思考网络结果才能连接过去？

![image-20200922002604660](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922002604660.png)

## 可视化

- portainer(先用这个)

```shell
docker run -d -p 8088:9000 \
--restart=always -v /var/run/docker.sock:/var/run/docker.sock --privileged=true portainer/portainer
```

- Rancher(CI/CD再用)



什么portainer

Docker图形化界面管理！提供一个后台面板供我们操作！

```shell
docker run -d -p 8088:9000 \
--restart=always -v /var/run/docker.sock:/var/run/docker.sock --privileged=true portainer/portainer
```

访问测试:外网:8088

![image-20200922003629870](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922003629870.png)

选择本地

![image-20200922003758104](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922003758104.png)

![image-20200922004101925](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922004101925.png)

进入之后的面板

![image-20200922004253534](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922004253534.png)

可视化面积我们平时不会使用,大家自己测试玩玩即可！

# Dock镜像讲解

## 镜像是什么

镜像是一种轻量级、可执行的独立软件包,用来打包软件运行环境和基于运行环境开发的软件,它包含运行某个软件所需的所有内容,包括代码、运行时、库、环境变量和配置文件.

所有的应用,直接打包docker镜像,就可以直接跑起来！

**如何得到镜像:**

- 从远程仓库下载
- 朋友拷贝给你
- 自己制作一个镜像DockerFile

## Docker镜像加载原理

> UnionFS ( 联合文件系统 )

我们下载的时候看到的一层层就是这个！

UnionFS ( 联合文件系统 ):Union文件系统 ( UnionFS )是一种分层、轻量级并且高性能的文件系统,它支持对文件系统的修改作为一次提交来一层层的叠加,同时可以将不同目录挂载到同一个虚拟文件系统下(unite several directiories into a single virtual filesystem).Union文件系统是Docker镜像的基础.镜像可以通过分层来进行继承,基于基础镜像 ( 没有父镜像 ),可以制作各种具体的应用镜像.

特性:一次同时加载多个文件系统,但从外面看起来,只能看到一个文件系统,联合加载会把各层文件系统叠加起来,这样最终的文件系统会包含所有底层的文件和目录.

> Dock镜像加载原理

docker的镜像实际上由一层一层的文件系统组成,这种层级的文件系统UnionFS.

bootfs ( boot file system ) 主要包含bootloader和kernel,bootolader主要是引导加载kernel,Linux刚启动时会加载bootfs文件系统,在Docker镜像的最底层是bootfs.这一层与我典型的Linux/Unix系统是一样的,包含boot加载器和内核.当boot内核完成之后整个内核就都在内存中了,此时内存的使用权已由bootfs转交内核,此时系统会卸载bootfs.



rootfs ( root file system ) ,在bootfs之上,包含的就是典型Linux系统中的/dev、/proc、/bin、/etc等标准目录和文件.rootfs就是各种不同的操作系统发行版,比如Ubuntu , Centos等等.

![image-20200922010643501](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922010643501.png)

平时我们安装进虚拟机的CentOs都是好几个G,为什么Docker这里才200M?

![image-20200922011326453](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922011326453.png)

对于一个精简的OS,rootfs可以很小,只需要包含最基本的命令,工具和程序库就可以了,因为底层直接用Host的kernel,自己只需要提供rootfs就可以了.由此可见对于不同的linux发行版,bootfs基本是一致的,rootfs会有差别,因此不同的发行版可以公用bootfs.

虚拟机是分钟级别,容器是秒级!

## 分层理解

> 分层理解

我们可以去下载一个镜像,注意观察下载的日志输出,可以看到是一层一层的在下载！

![image-20200922011918972](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922011918972.png)

思考:为什么Docker镜像要采用这种分层的结构呢？

最大的好处,我觉得莫过于是资源共享了！比如有多个镜像都从相同的Base镜像构建而来,那么宿主机只需在磁盘上保留一份base镜像,同时内存中也只需要加载一份base镜像,这样就可以为所有的容器服务了,而且镜像的每一层都可以共享.

查看镜像分层的方式可以通过 docker image inspect 命令！

```shell
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker image inspect centos
[
    {
        "Id": "sha256:0d120b6ccaa8c5e149176798b3501d4dd1885f961922497cd0abef155c869566",
        "RepoTags": [
            "centos:latest"
        ],
        "RepoDigests": [
            "centos@sha256:76d24f3ba3317fa945743bb3746fbaf3a0b752f10b10376960de01da70685fbd"
        ],
        "Parent": "",
        "Comment": "",
        "Created": "2020-08-10T18:19:49.837885498Z",
        "Container": "3b04ecd9fb2d3f921f12d858edf5f3a6aa7c36c8e1e6f74bd32555fd4d7f7da2",
        "ContainerConfig": {
            "Hostname": "3b04ecd9fb2d",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/bin/sh",
                "-c",
                "#(nop) ",
                "CMD [\"/bin/bash\"]"
            ],
            "ArgsEscaped": true,
            "Image": "sha256:69587a438b2c9b803db8ed4f6e6b5abce25a6b8ec2583a394807cf82bfd23693",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "org.label-schema.build-date": "20200809",
                "org.label-schema.license": "GPLv2",
                "org.label-schema.name": "CentOS Base Image",
                "org.label-schema.schema-version": "1.0",
                "org.label-schema.vendor": "CentOS"
            }
        },
        "DockerVersion": "18.09.7",
        "Author": "",
        "Config": {
            "Hostname": "",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/bin/bash"
            ],
            "ArgsEscaped": true,
            "Image": "sha256:69587a438b2c9b803db8ed4f6e6b5abce25a6b8ec2583a394807cf82bfd23693",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "org.label-schema.build-date": "20200809",
                "org.label-schema.license": "GPLv2",
                "org.label-schema.name": "CentOS Base Image",
                "org.label-schema.schema-version": "1.0",
                "org.label-schema.vendor": "CentOS"
            }
        },
        "Architecture": "amd64",
        "Os": "linux",
        "Size": 215102299,
        "VirtualSize": 215102299,
        "GraphDriver": {
            "Data": {
                "MergedDir": "/var/lib/docker/overlay2/69da5c6bed605fc9a0bf0624a6290de42cda24892caa8618e04317dbcdeb7caf/merged",
                "UpperDir": "/var/lib/docker/overlay2/69da5c6bed605fc9a0bf0624a6290de42cda24892caa8618e04317dbcdeb7caf/diff",
                "WorkDir": "/var/lib/docker/overlay2/69da5c6bed605fc9a0bf0624a6290de42cda24892caa8618e04317dbcdeb7caf/work"
            },
            "Name": "overlay2"
        },
        "RootFS": {
            "Type": "layers",
            "Layers": [
                "sha256:291f6e44771a7b4399b0c6fb40ab4fe0331ddf76eda11080f052b003d96c7726"
            ]
        },
        "Metadata": {
            "LastTagTime": "0001-01-01T00:00:00Z"
        }
    }
]

```

理解:

所有的Docker镜像都起始于一个基础镜像层,当进行修改或增加新的内容时,就会在当前镜像层之上,创建新的镜像层.

举一个简单的例子,假如基于Ubuntu Linux 16.04 创建一个新的镜像,这就是新镜像的第一层；如果在该镜像中添加Python包,就会在基础镜像层上创建第二个镜像层；如果继续添加一个安全补丁,就会创建第三个镜像层.

该镜像当前已经包含3个镜像层,如下图所示(这只是一个用于演示的很简单的例子).

![image-20200922012830742](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922012830742.png)

在添加额外镜像层的同时,镜像始终保持是当前所有镜像的组合,理解这一点非常重要.下图中举了一个简单的例子,每个镜像层包含3个文件,而镜像包含了来自两个镜像层的6个文件.

![image-20200922013129804](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922013129804.png)

上图中的镜像层路之前图中的略有区别,主要目的是便于展示文件.

下图中展示了一个稍微复杂的三层镜像,在外部看来整个镜像只有6个文件,这是因为最上层中的文件7是文件5的一个更新版本.

![image-20200922013408112](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922013408112.png)

这种情况下,上层镜像层中的文件覆盖了底层镜像层中的文件,这样就使得文件的更新版本作为一个新镜像层添加到镜像当中.

Docker通过存储引擎( 新版本采用快照机制 ) 的方式来实现镜像层堆栈,并保证多镜像层对外展示为统一的文件系统.

Linux 上可用的存储引擎 有AUFS、Overlay2、Device Mapper、Btrfs 以及ZFS. 顾名思义,每种存储引擎都基于 Linux 中对应的文件系统或者块设备技术,并且每种存储引擎都有其独有的性能特点.

Docker 在Windows 上仅支持 windowsfiter 一种存储引擎,该引擎基于 NTFS 文件系统之上实现分层和Cow[1].

下图展示了与系统显示相同的三层镜像.所有镜像层堆叠并合并,对外提供统一的视图.

![image-20200922014156419](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922014156419.png)

> 特点

Docker镜像都是只读的.当容器启动时,一个新的可写层被加载到镜像的顶部！

这一层就是我们通常说的容器层,容器之下的都叫镜像层！

![image-20200922014733704](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922014733704.png)

如何提交一个自己的镜像

## commit镜像

```shell
docker commit 提交容器成为一个新的副本

docker commit -m="提交的描述信息" -a="作者" 容器id 目标镜像名:[TAG]
```

实战测试

```shell
# 1、启动一个默认的tomcat

# 2、发现这个默认的tomcat 是没有webapps应用,镜像的原因,官方的镜像默认 webapps下面是没有文件的！

# 3、我自己拷贝进去了基本的文件
# 4、将我们操作过的容器通过commit提交为一个镜像！我们以后就使用我们修改过的镜像即可这就是我们自己的一个修改的镜像
```

![image-20200922015901933](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922015901933.png)

学习方式说明:理解概念,但是一定要实践,最后实践和理论合一次搞定这个知识！

```shell
如果你想要保存当前容器的状态,就可以通过commit提交,获得一个镜像.
就好比我们以前学习VM时候,快照！
```

到了这里才算是入门Docker！认真吸收练习,该休息！



# 容器数据卷

## 什么是容器数据卷

docker的理念回顾

将应用和环境打包成一个镜像！

数据？如果数据都在容器中,那么我们容器删除,数据就会丢失！  ==需求 : 数据可以持久化==

MySQL,容器删了,删库跑路！  ==需求:MySQL数据可以存储在本地！==

容器之间可以一个数据共享的技术！Docker容器中产生的数据,同步到本地！

这就是卷技术！目录的挂载,将我们容器内的目录,挂载到Linux上面！

![image-20200922021548015](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922021548015.png)

总结一句话:容器的持久化和同步操作！

## 使用数据卷

> 方式一: 直接使用命令来挂载 -v

``` shell
docker run -it -v 主机目录,容器内目录
# 测试
docker run -it -v /home/ceshi:/home centos /bin/bash

# 启动起来时候我们可以通过docker inspect 容器id 
```

![image-20200922030017880](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922030017880.png)

![image-20200922030322922](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922030322922.png)

测试文件的同步

再来测试

1、 停止容器

2、宿主机上修改文件

3、启动容器

4、容器内的数据依旧是同步的！

![image-20200922030640637](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922030640637.png)



好处:我们以后修改只需要在本地修改即可,容器内会自动同步！

## 实战:安装MySQL

思考:MySQL的数据持久化的问题

```shell
#获取镜像
$ [root@iZm5egx0inbsssu7xq22z7Z ~]# docker pull mysql:5.7

#运行容器,需要做数据挂载！#安装启动mysql

# 官方测试:
$ docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:tag

# 启动我们的:
-d 后台运行
-p 端口映射
-v 卷挂载
-e 环境配置
--name 容器名字
[root@iZm5egx0inbsssu7xq22z7Z /]# docker run -d -p 3344:3306 -v /docker_/mysql/conf:/etc/mysql/conf.d -v /docker_/mysql/data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456   --name mysql01 mysql:5.7

#启动成功之后 ,我们在本地使用 sqlyog 来接测试一下
#sqlyog-连接到服务器到3344 ----3344 和容器内的3306映射,这个时候我们就可以连接上了！

```

## 具名和匿名挂载

```shell
# 匿名挂载
-v 容器内路径！
docker run -d -P --name nginx01 -v /etc/nginx nginx

# 查看所有的 volume 情况
docker volume ls

#具名挂载
[root@iZm5egx0inbsssu7xq22z7Z docker_]# docker run -d -P --name nginx02 -v /docker_/juming-nginx:/etc/nginx nginx

#通过 -v 卷名:容器内路径
#查看一下这个卷
```

![image-20200922035744650](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922035744650.png)

所有的docker容器内的卷,没有指定目录的情况下都是在`/var/lib/docker/volumes/xxxx/_data`

我们通过具名挂载可以方便的找到我们的一个卷,大多数情况在使用的具名挂载

```shell
#如何确定是具名挂载还是匿名挂载,还是指定路径挂载！
-v 容器内路径	#匿名挂载
-v 卷名:容器内路径 #具名挂载
-v /宿主机路径:容器内路径 #指定路径
```

拓展:

``` shell
#通过 -v 容器内路径:ro rw 改变读写权限
ro readonly		#可读 
rw readwrite 	#可读可写

#一旦这个了设置容器权限 容器对我们挂载出来的内容就有限定！
docker run -d -P --name nginx2 -v juming-nginx:/etc/nginx:ro nginx
docker run -d -P --name nginx2 -v juming-nginx:/etc/nginx:rw nginx

#ro 只要看到ro就说明这个路径只能通过宿主机操作,容器内部是无法操作！

```

## 初识DockerFile

Dockfile就是用来构建docker镜像的构建文件！命令脚本！先体验一下！

通过这个脚本可以生成镜像,镜像是一层一层的,脚本一个个的命令,每个命令都是一层！

```shell
# 创建一个dockerfile文件,名字可以随机 建议Dockerfile
# 文件中的内容 指令(大写) 参数
FROM centos
  
VOLUME ["volume01","volume02"]  #匿名挂载

CMD echo "----end----"

CMD /bin/bash

# 这里的每个命令,就是镜像的一层
```

```shell
#启动自己写的容器
```

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922152841859.png)

这个卷和外部有一定同步的目录！

![image-20200922153413259](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922153413259.png)

查看一下卷挂载的路径

![image-20200922153345480](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922153345480.png)

测试一下刚才的文件是否同步出去了！

这种方式我们未来使用的十分多,因为我们通常会构建自己的镜像！

假设构建镜像时候没有挂载卷,要手动镜像 -v 卷名:容器内路径！





## 数据卷容器

多个 mysql 同步数据！

![image-20200922154845657](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922154845657.png)



```shell
#启动3个容器,通过我们刚才自己的写镜像启动
```

![image-20200922155206994](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922155206994.png)

```shell
[root@iZm5egx0inbsssu7xq22z7Z _data]# docker run -it --name docker02 --volumes-from docker01 root/centos:1.0 

```

![image-20200922155626434](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922155626434.png)

![image-20200922155647907](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922155647907.png)

![image-20200922155937415](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922155937415.png)

``` shell
# 测试: 可以删除docker01,查看一下docker02和docker03是否还可以访问这个文件
# 测试依旧可以访问
```



![image-20200922160212099](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922160212099.png)

多个mysql实现数据共享

``` shell
[root@iZm5egx0inbsssu7xq22z7Z /]# docker run -d -p 3344:3306 -v /etc/mysql/conf.d -v /var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456   --name mysql01 mysql:5.7

[root@iZm5egx0inbsssu7xq22z7Z /]# docker run -d -p 3344:3306 -v /etc/mysql/conf.d -v /var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456   --name mysql02 --volumes-from mysql01 mysql:5.7

#这个时候,可以实现两个容器数据同步！
```

结论:

容器之间配置信息的传递,数据卷容器的生命周期一直持续到没有容器使用为止.

但是一旦你持久化到了本地,这个时候,本地的数据是不会删除的.

# DockerFile

##  介绍Dockerfile

>  Docker的精髓

docker用来构建docker镜像的文件！

构建步骤:

1、编写一个 dockerfile 文件

2、docker build 构建成为一个镜像

3、docker run 运行镜像

4、docker push 发布镜像 (Dcokerhub、阿里云镜像仓库！)

![image-20200922161816032](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922161816032.png)

![image-20200922161857116](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922161857116.png)

很多官方镜像都是基础包,很多功能没有,我们通常会自己搭建自己的镜像！

官方既然可以制作镜像,那我们也可以！

## DockerFile构建过程

**基础知识:**

1、 每个保留关键字( 指令 ) 都是必须是大写字母

2、 执行从上到下顺序执行

3、 #表示注释

4、 每一个指令都会创建提交一个新的镜像层,并提交！

![image-20200922162604267](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922162604267.png)

dockerfile是面向开发的,我们以后要发布项目,做镜像,就需要编写dockerfile文件,这个文件十分简单！

docker镜像逐渐成为企业交付的标准,必须掌握！

**步骤 : 开发 , 部署 , 运维 ...缺一不可！**

DockerFile : 构建文件,定义了一切的步骤,源代码

DockerImages : 通过 DockerFile 构建生成的镜像 , 最终发布和运行的产品 , 

Docker容器 : 容器就是镜像运行起来提供服务器

## DockerFile的指令

以前的话我们就是使用别人的,现在我们知道了这些指令后,我们来练习自己写一个镜像！

``` shell
FROM 		# 基础镜镜像,一切从这里开始构建
MAINTIANER	# 镜像是谁写的,姓名+邮箱
RUN			# 镜像构建的时候需要运行命令
ADD			# 步骤: tomcat镜像 , 这个tomcat压缩包！
WORKDIR		# 镜像的工作目录
VOLUME		# 挂载的目录
EXPOSE		# 保留端口配置
CMD			# 指定这个窗口启动的时候要运行的命令,只有最后一个会生效,可被替代
ENTRYPIONT	# 指定这个窗口启动的时候要运行的命令,可以追加命令
ONBUILD		# 当构建一个被继承 DockerFile 这个时候就会运行 ONBUILD 的指令 . 触发指令 .
COPY		# 类似 ADD ,将我们文件拷贝到镜像中
ENV			# 构建的时候设置环境变量！
```



![image-20200922163152302](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922163152302.png)

实战测试

Docker Hub 中 99% 镜像都是从这个基础镜像过来的 FROM scratch , 然后配置需要的软件和配置来进行的构建

![image-20200922164652221](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922164652221.png)

> 创建一个自己的centos



```shell
# 1、 编写DockerFile的文件
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# cat mydockerfile 
FROM centos
MAINTAINER weqq<1515817@qq.com>

ENV MYPATH /usr/local
WORKDIR $MYPATH 

RUN yum -y install vim 
RUN yum -y install net-tools

EXPOSE 80

CMD echo $MYPATH
CMD echo "----end----"
CMD /bin/bash

# 2、 通过这个文件构建镜像
# 命令 docker build -f dockerfile文件路径 -t 镜像名:[TAG]
# docker build -f mydockerfile -t mycentos:0.1 .

Successfully built 4750cfae1514
Successfully tagged mycentos:0.1

# 测试运行


```

对比:之前的原生的centos

![image-20200922171432419](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922171432419.png)

我们增加之后的镜像

![image-20200922171506988](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922171506988.png)

我们可以列出本地进行的更改历史

![image-20200922171938862](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922171938862.png)



我们平时拿到一个镜像,可以研究一下它是怎么做的了？

> CMD 和ENTRYPOINT 区别

CMD			# 指定这个窗口启动的时候要运行的命令,只有最后一个会生效,可被替代
ENTRYPIONT	# 指定这个窗口启动的时候要运行的命令,可以追加命令

测试CMD

``` shell
# 编写 dockerfile 文件
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# vim dockerfile-cmd-test
FROM centos
CMD ["ls","-a"]

# 构件镜像
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# docker build -f dockerfile-cmd-test -t cmdtest .

# run运行 发现我们的ls -a 命令生效
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# docker run 971766307859
.
..
.dockerenv
bin
dev
etc
home
lib
lib64
lost+found
media
mnt
opt
proc
root
run
sbin
srv
sys
tmp
usr
var

#想追加一个命令 -l ls -al
root@iZm5egx0inbsssu7xq22z7Z dockerfile]# docker run 971766307859 -l
docker: Error response from daemon: OCI runtime create failed: container_linux.go:345: starting container process caused "exec: \"-l\": executable file not found in $PATH": unknown.

#cmd的清理下 -l 替换了CMD ["ls","-a"],-l 不是命令所以报错！

```

测试 ENTRYPOINT

```shell
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# 
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# vim dockerfile-cmd-entrypoint
FROM centos
ENTRYPOINT  ["ls","-a"]
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# docker build -f dockerfile-cmd-entrypoint -t entoryponit-test .
Sending build context to Docker daemon  4.096kB
Step 1/2 : FROM centos
 ---> 0d120b6ccaa8
Step 2/2 : ENTRYPOINT ["ls","-a"]
 ---> Running in 63ae0956f8ae
Removing intermediate container 63ae0956f8ae
 ---> 32f3b93e59c9
Successfully built 32f3b93e59c9
Successfully tagged entoryponit-test:latest
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# docker run 32f3b93e59c9
.
..
.dockerenv
bin
dev
etc
home
lib
lib64
lost+found
media
mnt
opt
proc
root
run
sbin
srv
sys
tmp
usr
var
[root@iZm5egx0inbsssu7xq22z7Z dockerfile]# docker run 32f3b93e59c9 -l
total 0
drwxr-xr-x   1 root root   6 Sep 22 09:33 .
drwxr-xr-x   1 root root   6 Sep 22 09:33 ..
-rwxr-xr-x   1 root root   0 Sep 22 09:33 .dockerenv
lrwxrwxrwx   1 root root   7 May 11  2019 bin -> usr/bin
drwxr-xr-x   5 root root 340 Sep 22 09:33 dev
drwxr-xr-x   1 root root  66 Sep 22 09:33 etc
drwxr-xr-x   2 root root   6 May 11  2019 home
lrwxrwxrwx   1 root root   7 May 11  2019 lib -> usr/lib
lrwxrwxrwx   1 root root   9 May 11  2019 lib64 -> usr/lib64
drwx------   2 root root   6 Aug  9 21:40 lost+found
drwxr-xr-x   2 root root   6 May 11  2019 media
drwxr-xr-x   2 root root   6 May 11  2019 mnt
drwxr-xr-x   2 root root   6 May 11  2019 opt
dr-xr-xr-x 121 root root   0 Sep 22 09:33 proc
dr-xr-x---   2 root root 162 Aug  9 21:40 root
drwxr-xr-x  11 root root 163 Aug  9 21:40 run
lrwxrwxrwx   1 root root   8 May 11  2019 sbin -> usr/sbin
drwxr-xr-x   2 root root   6 May 11  2019 srv
dr-xr-xr-x  13 root root   0 Sep 22 09:33 sys
drwxrwxrwt   7 root root 145 Aug  9 21:40 tmp
drwxr-xr-x  12 root root 144 Aug  9 21:40 usr
drwxr-xr-x  20 root root 262 Aug  9 21:40 var

```

Docker中很多命令都十分的相似,我们需要了解它们的区别,我们最好的学习就是对比他们然后测试效果！

## 实战:Tomcat镜像

1、 准备镜像文件 tomcat压缩包,jdk的压缩包！

![image-20200922174016326](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922174016326.png)

2、 编写dockerfile文件 , 官方命名 ` Dockerfile` ,bulid 会自动寻找这个文件,就不需要 -f指定了！

```shell
FROM centos
MAINTAINER weqq<1515817@qq.com>

COPY readme.txt /usr/local/readme.txt
ADD jdk-8ull-linux.x64.tar.gz /usr/local/
ADD capche-tomcat-9.0.22.tar.gz /usr /local/

RUN yum -y install vim

ENV MYPATH /usr/local
WORKDIR $MYPATH

ENV JAVA_HOME /usr/local/jdk1.8.0_11
ENV CLSSPATH $JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV CATAINA_HOME /usr/local/apache-tomcat-9.0.22
ENV CATAINA_BASH /usr/local/apache-tomcat-9.0.22
ENV PATH $PATH:$JAVA_HOME/bin:$CATAINA_HOME/lib:$CATALINA_HOME/bin

EXPOSE 8080

CMD /usr/local/apache-tomcat-9.0.22bin/startup.sh && tail -F /url/local/apache-tomcat-9.0.22/bin/logs/cataline.out

```



3、 构建镜像

```shell
# docker build -t diytomcat .
```

4、 启动镜像

5、访问测试

6、发布项目 ( 由于做了卷挂载,我们直播在本地编写项目就可以发布了！)



我们以后开发的步骤:需要掌握Dockerfile的编写！我们之后的一切都是使用docker镜像来发布运行！



## 发布自己的镜像

> DockerHub

1、地址:https://hub.docker.com/ 注册自己的帐号

2、确定这个帐号可以登录

3、在我们服务器上提交自己的镜像

``` shell
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker login --help

Usage:	docker login [OPTIONS] [SERVER]

Log in to a Docker registry.
If no server is specified, the default is defined by the daemon.

Options:
  -p, --password string   Password
      --password-stdin    Take the password from stdin
  -u, --username string   Username

[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker login -u 1515817
Password: 
WARNING! Your password will be stored unencrypted in /root/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded

```

4、登录完毕后就可以提交镜像了,就是一步 docker push

```shell

# push 自己的镜像到服务器上！
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker push 1515817/mycentos:0.1 
The push refers to repository [docker.io/1515817/mycentos]
An image does not exist locally with the tag: 1515817/mycentos
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker push 1515817/mycentos:0.2
The push refers to repository [docker.io/1515817/mycentos]
An image does not exist locally with the tag: 1515817/mycentos
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker push 1515817/mycentos:0.3
The push refers to repository [docker.io/1515817/mycentos]
An image does not exist locally with the tag: 1515817/mycentos
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker push 1515817/mycentos:0.4
The push refers to repository [docker.io/1515817/mycentos]
An image does not exist locally with the tag: 1515817/mycentos
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker push diycentos
The push refers to repository [docker.io/library/diycentos]
An image does not exist locally with the tag: diycentos
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker push mycentos
The push refers to repository [docker.io/library/mycentos]
7c876a2db519: Preparing 
b2951fb594cb: Preparing 
291f6e44771a: Preparing 
denied: requested access to the resource is denied #拒绝

# push镜像的问题？
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker push 1515817/mycentos:0.1 

# 解决:增加一个标签
docker tag 4750cfae1514 1515817/centos:1.0

# docker psuh 上去即可！ 自己发布的镜像尽量带上版本号
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker push 1515817/centos:1.0
The push refers to repository [docker.io/1515817/centos]
7c876a2db519: Pushing [==============>                                    ]  6.736MB/22.78MB
b2951fb594cb: Pushing [===============>                                   ]  17.85MB/57.24MB
291f6e44771a: Pushing [====>                                              ]  17.45MB/215.1MB

```

提交的时候也是按照镜像的层级来进行提交的！



> 阿里云镜像服务上

1. 登录阿里云
2. 找到容器镜像服务
3. 创建命名空间
4. ![image-20200922183139818](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922183139818.png)
5. 创建容器镜像

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922183724737.png)



![image-20200922183845612](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922183845612.png)

```shell

```

阿里云容器镜像的就参考官方地址！





##  小结:

![image-20200922190412033](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922190412033.png)



> 一夜回到解放前  

```shell
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker rm -f $(docker ps -aq)
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker rmi -f $(docker images -aq)
```



# Docker 网络

## 理解Docker0

> 测试

![image-20200922192459851](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922192459851.png)



三个网络

#问题:docker 是如何处理容器网络访问的？

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922192628137.png)

```shell
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker run -d -P --name tomcat01 tomcat

# 查看容器的内容网络地址:ip addr .发现容器启动的时候会得到 一个eth0@if125 ip地址,docker分配的！

[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker exec -it tomcat01 ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
124: eth0@if125: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default 
    link/ether 02:42:ac:11:00:02 brd ff:ff:ff:ff:ff:ff link-netnsid 0
    inet 172.17.0.2/16 brd 172.17.255.255 scope global eth0
       valid_lft forever preferred_lft forever
       
# 思考,Linux 能不能ping 能容器内部！
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# ping 172.17.0.2
PING 172.17.0.2 (172.17.0.2) 56(84) bytes of data.
64 bytes from 172.17.0.2: icmp_seq=1 ttl=64 time=0.074 ms
64 bytes from 172.17.0.2: icmp_seq=2 ttl=64 time=0.055 ms
64 bytes from 172.17.0.2: icmp_seq=3 ttl=64 time=0.059 ms
64 bytes from 172.17.0.2: icmp_seq=4 ttl=64 time=0.057 ms
64 bytes from 172.17.0.2: icmp_seq=5 ttl=64 time=0.058 ms
64 bytes from 172.17.0.2: icmp_seq=6 ttl=64 time=0.056 ms
64 bytes from 172.17.0.2: icmp_seq=7 ttl=64 time=0.055 ms
64 bytes from 172.17.0.2: icmp_seq=8 ttl=64 time=0.054 ms

#Linux 可以ping 通 docker 容器内部

```

> 原理

1. 我们每安装一个docker容器,docker就会给docker容器分配一个ip,我们只要安装了docker,就会有一个网卡docker0 桥接模式,使用的技术是evth-pair技术！
2. 再次测试ip addr

![image-20200922193643433](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922193643433.png)

3. 在启动一个容器测试,发现又多了一对网卡！

   ![image-20200922194007209](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922194007209.png)

``` shell 
# 我们发现这个容器带来网卡,都是一对对的
# evth-pair 就是一对的虚拟设备接口,他们都是成对出现的,一段连着协议,一段彼此相连
# 正因为有这个特性,evth-pair 充当一个桥梁,连接各种虚拟网络设备的
# OpenStrac,Docker容器之间的连接,ovs的连接,都是使用 evth-pair 技术
```

4. 我们来测试下tomcat01和tomcat02是否可以ping

![image-20200922194604358](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922194604358.png)

绘制一个网络模型图:

![image-20200922195841245](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922195841245.png)

结论:tomcat01和tomcat02是公用的一个路由器,docker0.

所有的容器不指定网络的情况下,都是docker0路由的,docker会给我们的容器分配一个默认的可用ip

> 小结

Docker使用的是Linux的桥接,宿主机是一个Docker容器的网桥 docker0.

![image-20200922201412018](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922201412018.png)

Docker中的所有网络接口都是虚拟的.虚拟的转发效率高！( 内网 传送文件！)

只要容器删除,对应网格一对就没了！



![image-20200922203149500](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922203149500.png)

## --link



>思考一个场景,我们编写了一个微服务,database url=ip: 项目不重启,数据库ip换了,我们希望可以处理这个问题,可以名字来进行访问容器？

mysql ip 

``` shell
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker exec -t tomcat01 ping tomcat02
ping: tomcat02: Name or service not known

# 如何可以解决呢？

# 通过--link 即可以解决了网络连通问题
[root@iZm5egx0inbsssu7xq22z7Z ~]# docker run -d -P --name tomcat03 --link tomcat02 tomcat

# 反问可以ping通？
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker exec -t tomcat02 ping tomcat03
ping: tomcat02: Name or service not known
```



![image-20200922203325402](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922203325402.png)



其实这个tomcat03就是在本地配置了tomcat022的配置？

``` shell
#查看 host配置 ,在这里原理发现！
```

![image-20200922203948249](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922203948249.png)

--link 就是我们在host配置中增加了一个172.17.0.3	tomcat02 375e1caeb05c 

![image-20200922204141618](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922204141618.png)

我们现在玩Docker 已经不建议使用 --link 了 ！

自定义网络！ 不适用docker0!

docker0问题:他不支持容器名连接访问！

## 自定义网络

![image-20200922204403308](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922204403308.png)

网络模式

bridege : 桥接 docker (默认,自己床架也使用bridege  模式)

none : 不配置网络

host : 和宿主机共享网络

container : 容器网络连通！(用的少！局限很大)

测试

``` shell
# 我们直接启动命令 --net bridge 而这个就是我们的docker0
docker run -d -P --name tomcat01  tomcat
docker run -d -P --name tomcat01 --net bridge tomcat

# docker0特点:默认:域名不能访问, --link可以打通连接！

#我们可以自定义一个网络！
# --driver bridge 
# --subnet 192.168.0.0/16 
# --gateway 192.168.0.1 
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker network  create --driver bridge --subnet 192.168.0.0/16 --gateway 192.168.0.1 mynet
b8b8ae0720a96e4b47833f2f41ab984ee1c34b00a14c8d2fdcfc5a53088370a0

[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker network ls
NETWORK ID          NAME                DRIVER              SCOPE
752a7c37e068        bridge              bridge              local
6346777efaec        host                host                local
b8b8ae0720a9        mynet               bridge              local
b717d12cbdad        none                null                local
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# 


```

我们自己的网络就创建好了！

![image-20200922205450589](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922205450589.png)

```shell
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker run -d -P --name tomcat-net-01 --net mynet tomcat
96557ceab5e0af2416e71ca7d59875decf245285575a9baea2366f56206b7b93
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker run -d -P --name tomcat-net-02 --net mynet tomcat
2149dfa108982ac17a614b53f3c782b18e5339e15903a7a5e50d340bb8abf2ae
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker run -d -P --name tomcat-net-03 --net mynet tomcat
30557ed96e1ce22e00dfa3af2da0c17dfe58951fffc3d40ae223f7fe77dd0b4d
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker network inspect mynet
[
    {
        "Name": "mynet",
        "Id": "b8b8ae0720a96e4b47833f2f41ab984ee1c34b00a14c8d2fdcfc5a53088370a0",
        "Created": "2020-09-22T20:52:28.698630591+08:00",
        "Scope": "local",
        "Driver": "bridge",
        "EnableIPv6": false,
        "IPAM": {
            "Driver": "default",
            "Options": {},
            "Config": [
                {
                    "Subnet": "192.168.0.0/16",
                    "Gateway": "192.168.0.1"
                }
            ]
        },
        "Internal": false,
        "Attachable": false,
        "Ingress": false,
        "ConfigFrom": {
            "Network": ""
        },
        "ConfigOnly": false,
        "Containers": {
            "2149dfa108982ac17a614b53f3c782b18e5339e15903a7a5e50d340bb8abf2ae": {
                "Name": "tomcat-net-02",
                "EndpointID": "fcc89a5879fd8f5f8edcd19461a0aa9bf68dc02b73f05882654383794ae45cf3",
                "MacAddress": "02:42:c0:a8:00:03",
                "IPv4Address": "192.168.0.3/16",
                "IPv6Address": ""
            },
            "30557ed96e1ce22e00dfa3af2da0c17dfe58951fffc3d40ae223f7fe77dd0b4d": {
                "Name": "tomcat-net-03",
                "EndpointID": "1758f4f209b7bb923482186fb5642b157a2da582a40c6fffdfe3090ba130cd2e",
                "MacAddress": "02:42:c0:a8:00:04",
                "IPv4Address": "192.168.0.4/16",
                "IPv6Address": ""
            },
            "96557ceab5e0af2416e71ca7d59875decf245285575a9baea2366f56206b7b93": {
                "Name": "tomcat-net-01",
                "EndpointID": "103105486eaaa04bef12e60f8eeddce3f9bdb75b46ef05dd4ca5e3ed50a7e44d",
                "MacAddress": "02:42:c0:a8:00:02",
                "IPv4Address": "192.168.0.2/16",
                "IPv6Address": ""
            }
        },
        "Options": {},
        "Labels": {}
    }
]


#再次测试ping连接

[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker exec -it tomcat-net-01 ping tomcat
tomcat01       tomcat-net-01  tomcat-net-02  tomcat-net-03  

# 现在不使用--link 也可以ping 名字了！
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker exec -it tomcat-net-01 ping tomcat-net-02
PING tomcat-net-02 (192.168.0.3) 56(84) bytes of data.
64 bytes from tomcat-net-02.mynet (192.168.0.3): icmp_seq=1 ttl=64 time=0.093 ms
64 bytes from tomcat-net-02.mynet (192.168.0.3): icmp_seq=2 ttl=64 time=0.082 ms
64 bytes from tomcat-net-02.mynet (192.168.0.3): icmp_seq=3 ttl=64 time=0.067 ms
64 bytes from tomcat-net-02.mynet (192.168.0.3): icmp_seq=4 ttl=64 time=0.089 ms
64 bytes from tomcat-net-02.mynet (192.168.0.3): icmp_seq=5 ttl=64 time=0.082 ms
64 bytes from tomcat-net-02.mynet (192.168.0.3): icmp_seq=6 ttl=64 time=0.082 ms
^C
--- tomcat-net-02 ping statistics ---
6 packets transmitted, 6 received, 0% packet loss, time 111ms
rtt min/avg/max/mdev = 0.067/0.082/0.093/0.012 ms
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker exec -it tomcat-net-01 ping 192.168.0.3
PING 192.168.0.3 (192.168.0.3) 56(84) bytes of data.
64 bytes from 192.168.0.3: icmp_seq=1 ttl=64 time=0.096 ms
64 bytes from 192.168.0.3: icmp_seq=2 ttl=64 time=0.078 ms
^C
--- 192.168.0.3 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 53ms
rtt min/avg/max/mdev = 0.078/0.087/0.096/0.009 ms

```

我们自定义的网络docker都已经帮我们维护好了对应的关系,推荐我们平时这样使用网络！



好处:

redis - 不同的集群使用不同的网络,保证集群是安全和健康的

mysql-- 不同的集群使用不同的网络,保证集群是安全和健康的！

## 网络连通

![image-20200922211151156](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922211151156.png)

![image-20200922211304475](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922211304475.png)

```shell
# 测试打通 tomcat01 - mynet 

# 连通之后就是将 tomcat01 放到了 mynet网络下？

# 一个容器 两个ip地址！ 阿里云服务:公网IP 私网IP


```

![image-20200922211426325](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922211426325.png)

``` shell
[root@iZm5egx0inbsssu7xq22z7Z docker-test-volume]# docker exec -it tomcat01 ping tomcat-net-01
PING tomcat-net-01 (192.168.0.2) 56(84) bytes of data.
64 bytes from tomcat-net-01.mynet (192.168.0.2): icmp_seq=1 ttl=64 time=0.074 ms
64 bytes from tomcat-net-01.mynet (192.168.0.2): icmp_seq=2 ttl=64 time=0.080 ms
64 bytes from tomcat-net-01.mynet (192.168.0.2): icmp_seq=3 ttl=64 time=0.086 ms
64 bytes from tomcat-net-01.mynet (192.168.0.2): icmp_seq=4 ttl=64 time=0.091 ms

```

![image-20200922211832797](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922211832797.png)

结论:假设要跨网络操作别人,就需要使用docker network connect 连通！...



## 实战:部署Redis集群

![image-20200922212613000](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922212613000.png)

> shell脚本

```shell
# 创建网卡
docker network create redis --subnet 172.38.0.0/16

# 通过脚本创建六个redis配置
for port in $(seq 1 6); \
do \
mkdir -p /mydata/redis/node-${port}/conf
touch /mydata/redis/node-${port}/conf/redis.conf
cat <<EOF >/mydata/redis/node-${port}/conf/redis.conf
port 6379
bind 0.0.0.0
cluster-enabled yes
cluster-config-file nodes.conf
cluster-node-timeout 5000
cluster-announce-ip 172.38.0.1${port}
cluster-announce-port 6379
cluster-announce-bus-port 16379
appendonly yes
EOF
done

$ for port in $(seq 1 6); \
do \
docker run -p 637${port}:6379 -p 1637${port}:16379 --name redis-${port} \
-v /mydata/redis/node-${port}/data:/data \
-v /mydata/redis/node-${port}/conf/redis.conf:/etc/redis/redis.conf \
-d --net redis --ip 172.38.0.1${port} redis:5.0.9-alpine3.11 redis-server /etc/redis/redis.conf 
done
$ docker exec -it redis-1 /bin/bash

$ redis-cli --cluster create 172.38.0.11:6379 172.38.0.12:6379 172.38.0.13:6379 172.38.0.14:6379 172.38.0.15:6379 172.38.0.16:6379 --cluster-replicas 1



##示例 
docker run -p 6371:6379 -p 16371:16379 --name redis-1 \
-v /mydata/redis/node-1/data:/data \
-v /mydata/redis/node-1/redis.conf:/etc/redis/redis.conf \
-d --net redis --ip 172.38.0.11 redis:5.0.9-alpine3.11 redis-server /etc/redis/redis.conf

docker run -p 6372:6379 -p 16372:16379 --name redis-2 \
-v /mydata/redis/node-2/data:/data \
-v /mydata/redis/node-2/redis.conf:/etc/redis/redis.conf \
-d --net redis --ip 172.38.0.12 redis:5.0.9-alpine3.11 redis-server /etc/redis/redis.conf

docker run -p 6376:6379 -p 16376:16379 --name redis-6 \
-v /mydata/redis/node-6/data:/data \
-v /mydata/redis/node-6/redis.conf:/etc/redis/redis.conf \
-d --net redis --ip 172.38.0.16 redis:5.0.9-alpine3.11 redis-server /etc/redis/redis.conf


redis-cli --cluster create 172.38.0.11:6379 172.38.0.12:6379 172.38.0.13:6379 172.38.0.14:6379 172.38.0.15:6379 172.38.0.16:6379 --cluster-replicas 1

# 创建集群
[root@iZm5egx0inbsssu7xq22z7Z conf]# for port in $(seq 1 6); \
> do \
> docker run -p 637${prot}:6379 -p 1637${port}:16379 --name redis-${port} \
> -v /mydata/redis/node-${port}/data:/data \
> -v /mydata/redis/node-${port}/conf/redis.conf:/etc/redis/redis.conf \
> -d --net redis --ip 172.38.0.1${port} redis:5.0.9-alpine3.11 redis-server /etc/redis/redis.conf 
> done^C
[root@iZm5egx0inbsssu7xq22z7Z conf]# docker rm -f $(docker ps -aq)
38eb1eb7f946
ece4c4a77640
f42515bcb672
05e087767562
86202dd1da9b
478d6491c42a
[root@iZm5egx0inbsssu7xq22z7Z conf]# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
[root@iZm5egx0inbsssu7xq22z7Z conf]# for port in $(seq 1 6); \
> do \
> docker run -p 637${port}:6379 -p 1637${port}:16379 --name redis-${port} \
> -v /mydata/redis/node-${port}/data:/data \
> -v /mydata/redis/node-${port}/conf/redis.conf:/etc/redis/redis.conf \
> -d --net redis --ip 172.38.0.1${port} redis:5.0.9-alpine3.11 redis-server /etc/redis/redis.conf 
> done
e8d9c5d3186e57506259936240109a701b141f9db535896bcfa5b48a05f0d901
3a61237527b3c8771d586f311c8b860b0b9d2df08cd7d8d1d1fd4bb2e41a7231
c9d73925539111ea78e90ca8b4b7e7da1435ac1ed775460bd0051b6ee6e8bb38
07d22ad2e7c58cf5d5d11dca1550273833fb7f681675404d31ee33641ff870ca
29c967866a22868d6b840f0278624711be38dc7cbe2ef9310884434c6f10ebe3
6207a0788f82b5b294b82d630a50ea1ae62ffd96ccf648d4d6cc4f5d0e41e83b
[root@iZm5egx0inbsssu7xq22z7Z conf]# docker ps
CONTAINER ID        IMAGE                    COMMAND                  CREATED             STATUS              PORTS                                              NAMES
6207a0788f82        redis:5.0.9-alpine3.11   "docker-entrypoint.s…"   12 seconds ago      Up 11 seconds       0.0.0.0:6376->6379/tcp, 0.0.0.0:16376->16379/tcp   redis-6
29c967866a22        redis:5.0.9-alpine3.11   "docker-entrypoint.s…"   13 seconds ago      Up 12 seconds       0.0.0.0:6375->6379/tcp, 0.0.0.0:16375->16379/tcp   redis-5
07d22ad2e7c5        redis:5.0.9-alpine3.11   "docker-entrypoint.s…"   13 seconds ago      Up 12 seconds       0.0.0.0:6374->6379/tcp, 0.0.0.0:16374->16379/tcp   redis-4
c9d739255391        redis:5.0.9-alpine3.11   "docker-entrypoint.s…"   14 seconds ago      Up 13 seconds       0.0.0.0:6373->6379/tcp, 0.0.0.0:16373->16379/tcp   redis-3
3a61237527b3        redis:5.0.9-alpine3.11   "docker-entrypoint.s…"   15 seconds ago      Up 14 seconds       0.0.0.0:6372->6379/tcp, 0.0.0.0:16372->16379/tcp   redis-2
e8d9c5d3186e        redis:5.0.9-alpine3.11   "docker-entrypoint.s…"   15 seconds ago      Up 14 seconds       0.0.0.0:6371->6379/tcp, 0.0.0.0:16371->16379/tcp   redis-1
[root@iZm5egx0inbsssu7xq22z7Z conf]# 
[root@iZm5egx0inbsssu7xq22z7Z conf]# docker exec -it redis-1 /bin/bash
OCI runtime exec failed: exec failed: container_linux.go:345: starting container process caused "exec: \"/bin/bash\": stat /bin/bash: no such file or directory": unknown
[root@iZm5egx0inbsssu7xq22z7Z conf]# docker exec -it redis-1 /bin/sh
/data # ls
appendonly.aof  nodes.conf
/data # redis-cli --cluster create 172.38.0.11:6379 172.38.0.11:6379 
*** ERROR: Invalid configuration for cluster creation.
*** Redis Cluster requires at least 3 master nodes.
*** This is not possible with 2 nodes and 0 replicas per node.
*** At least 3 nodes are required.
/data # redis-cli --cluster create 172.38.0.11:6379 172.38.0.12:6379 172.38.0.13:6379 172.38.0.14:6379 172.38.0.15:6379 172.38.0.16:6379 --cluster-replicas 1
>>> Performing hash slots allocation on 6 nodes...
Master[0] -> Slots 0 - 5460
Master[1] -> Slots 5461 - 10922
Master[2] -> Slots 10923 - 16383
Adding replica 172.38.0.15:6379 to 172.38.0.11:6379
Adding replica 172.38.0.16:6379 to 172.38.0.12:6379
Adding replica 172.38.0.14:6379 to 172.38.0.13:6379
M: f6360be3d3f26cc726d442e536cbd6fe43ad8148 172.38.0.11:6379
   slots:[0-5460] (5461 slots) master
M: 1e578f514c950dd49881b1c04aea50f06802f232 172.38.0.12:6379
   slots:[5461-10922] (5462 slots) master
M: 66f0fa5423fcba73a3fe127c7b14cc5605d073a7 172.38.0.13:6379
   slots:[10923-16383] (5461 slots) master
S: b6a90530966d6cd969925eb467f3a598e60a36a7 172.38.0.14:6379
   replicates 66f0fa5423fcba73a3fe127c7b14cc5605d073a7
S: 767bc6c31ba93ee30bb4a70797de63e9ce23bda1 172.38.0.15:6379
   replicates f6360be3d3f26cc726d442e536cbd6fe43ad8148
S: 348fdcac817706c16e6ceba0d1e31dd7028e91cc 172.38.0.16:6379
   replicates 1e578f514c950dd49881b1c04aea50f06802f232
Can I set the above configuration? (type 'yes' to accept): yes
>>> Nodes configuration updated
>>> Assign a different config epoch to each node
>>> Sending CLUSTER MEET messages to join the cluster
Waiting for the cluster to join
...
>>> Performing Cluster Check (using node 172.38.0.11:6379)
M: f6360be3d3f26cc726d442e536cbd6fe43ad8148 172.38.0.11:6379
   slots:[0-5460] (5461 slots) master
   1 additional replica(s)
S: b6a90530966d6cd969925eb467f3a598e60a36a7 172.38.0.14:6379
   slots: (0 slots) slave
   replicates 66f0fa5423fcba73a3fe127c7b14cc5605d073a7
M: 1e578f514c950dd49881b1c04aea50f06802f232 172.38.0.12:6379
   slots:[5461-10922] (5462 slots) master
   1 additional replica(s)
S: 348fdcac817706c16e6ceba0d1e31dd7028e91cc 172.38.0.16:6379
   slots: (0 slots) slave
   replicates 1e578f514c950dd49881b1c04aea50f06802f232
M: 66f0fa5423fcba73a3fe127c7b14cc5605d073a7 172.38.0.13:6379
   slots:[10923-16383] (5461 slots) master
   1 additional replica(s)
S: 767bc6c31ba93ee30bb4a70797de63e9ce23bda1 172.38.0.15:6379
   slots: (0 slots) slave
   replicates f6360be3d3f26cc726d442e536cbd6fe43ad8148
[OK] All nodes agree about slots configuration.
>>> Check for open slots...
>>> Check slots coverage...
[OK] All 16384 slots covered.
/data # 


```

![image-20200922222837875](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200922222837875.png)

我们使用了docker之后,所有的技术都会慢慢的变得简单起来！

# Springboot微服务打包Docker镜像

1. 构架springboot项目
2. 打包应用
3. 编写dockerfile
4. 构建镜像
5. 发布运行！

我们使用了Docker之后,给别人交付的就是一个镜像即可！

到了这里我们已经完全够用了Docker!

预告:如果有很多镜像,？？100个镜像？



企业

这里面都是集群部署！,一下来你们至少要准备6台阿里云服务器！一台服务器是搞不定的！

## Docker Compose

## Docker Swarm

## CI/CD之Jenkine



> `` 感谢狂神!!`` 