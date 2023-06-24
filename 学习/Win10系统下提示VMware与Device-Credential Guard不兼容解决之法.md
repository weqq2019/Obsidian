---
layout: post
title: Win10系统下提示VMware与Device/Credential Guard不兼容解决之法  
categories: [开发工具,VMware]
tags: VMware
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925003042833.png
---

![image-20200925003042833](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925003042833.png)

VMware是一个虚拟机软件，许多win10系统用户会在电脑中安装，然而有不少用户在安装VMware虚拟机之后，打开的时候提示VMware Workstation 与 Device/Credential Guard 不兼容，且在禁用Device/Credential Guard后才能运行VMware，该怎么办呢，本文就给大家分享一下Win10系统下提示VMware与Device/Credential Guard不兼容的具体解决方法。





#### 原因分析：

VMware和Hyper-V不兼容导致。

#### Win10专业版解决方法：

1、控制面板—程序——打开或关闭Windows功能，取消勾选Hyper-V，确定禁用Hyper-V服务。
2、之后重新启动计算机，再运行VM虚拟机即可。

#### Win10家庭版解决方法：

1、按下WIN+R打开运行，然后输入services.msc回车；
2、在服务中找到 HV主机服务，双击打开设置为禁用；
3、再打开Windows PowerShell（管理员）
4、运行命令：bcdedit /set hypervisorlaunchtype off；
5、再重新启动Win10系统就可以解决VM虚拟机打不开的问题了。

