---
layout: post
title:  使用Pycharm远程连接及管理Docker
categories: [开发工具,Docker]
tags:  Docker
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924060923342.png
---



![image-20200924060923342](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924060923342.png)

> 不容易....

为了使远端服务器上的Docker能与本机的Pychrm进行连接和通信，需要在远端服务器上做一些设置，允许docker能被指定IP访问。

### 开放远端连接

1. 修改配置文件
    执行命令： `vim /lib/systemd/system/docker.service`

   ![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924061237707.png)

   image.png

   

2. 将管理地址写入  /etc/profile
    执行命令：`echo 'export DOCKER_HOST=tcp://0.0.0.0:2375' >> /etc/profile`
    执行命令：`source /etc/profile`

3. 重启服务
    执行命令： `systemctl daemon-reload && systemctl restart docker`

### Pycharm中连接远端Docker

1. 打开docker连接窗口

   ![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924061215936.png)

   添加连接信息
    选择TCP连接，输入自己远端的IP地址和docker服务端口号，连接成功会在下方自动显示Connection successful,若连接失败可能是由于防火墙未开放端口引起的，需要先使用防火墙开启2375端口。

   ![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924061152335.png)

2. 连接成功
    连接成功后即可远程对Docker进行管理和信息显示。

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924061131559.png)

