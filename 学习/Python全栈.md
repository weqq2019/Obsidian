---
layout: post
title:  "Python全栈"
categories: Python
tags:  Python
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/7.png
---

* content
{:toc}
![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/7.png)

# Python

## 1 Linux基础

### 1.4 Linux常用命令

- 1.4.1 Linux命令格式与语法
- 1.4.2 whoami、who
- 1.4.3 date、cal、clear
- 1.4.2 su、passwd
- 1.4.5 man
- 1.4.6 目录介绍及pwd、cd、ls命令
- 1.4.7 cp、mv、mkdir、touch
- 1.4.8 rm、rmdir
- 1.4.9 cat、head、tail、more
- 1.4.10 用户及passwd文件、
shadow文件、群组及group文件
- 1.4.11 useradd、usermod、userdel、
groupadd、groupmod、groupdel
- 1.4.12 用户分类及文件权限、
chown、chgrp、chmod
- 1.4.13 tar、gip及gunzip、
bzip2及bunzip2
- 1.4.14 Vi编辑器
- 1.4.15 内核初始化和init初始化
- 1.4.16 runlevel、重启关闭系统、
单用户模式修改密码、救援模式
- 1.4.17 top和free
- 1.4.18 ps、pstree、kill、pkill、pgrep
- 1.4.19 fdisk、partprobe、
mkfs、e2label
- 1.4.20 mount、umount、mkswap、
swapon、df、du
- 1.4.21 ifconfig、ifup、
ifdown、ip、ping、setup

### 1.5 Linux常用服务

- 1.5.1 RPM软件包
- 1.5.2 Yum
- 1.5.3 Samba
- 1.5.4 Nginx
- 1.5.5 NFS
- 1.5.6 Crond

## 2 Python基础

### 2.2 编程基础

- 2.2.2 堆和栈
- 2.2.3 Python解释器原理

### 2.3 Python基础语法

- 2.3.1 Python编码规范
- 2.3.2 变量与赋值

### 2.4 流程控制

### 2.5 数据类型

### 2.6 运算

### 2.7 字符编码与转码

### 2.8 文件处理

### 2.9 函数和装饰器

### 2.10 迭代器和生成器

### 2.11 递归和反射

- 2.11.1 递归的特性
- 2.11.2 尾递归优化
- 2.11.3 反射的原理
- 2.11.4 hasattr、getattr、
setattr、delattr

### 2.12 内置方法

- 2.12.1 68个内置方法
- 2.12.2 copy和deepcopy
- 2.12.3 map、filter
- 2.12.4 functools

### 2.13 常用标准库

- 2.13.1 re模块
- 2.13.2 os、sys模块
- 2.13.3 subprocess模块
- 2.13.4 shutil、shelve、itertools模块
- 2.13.5 hashlib模块
- 2.13.6 logging日志模块
- 2.13.7 time、datetime模块
- 2.13.8 traceback模块
- 2.13.9 json、pickle、xml、
yaml、configparser模块
- 2.13.10 urlib模块
- 2.13.11 paramiko模块
- 2.13.12 random模块

### 2.14 面向对象编程

- 2.14.2 类和对象
- 2.14.4 面向对象三大特性:
封装、继承、多态
- 类的成员
- *2.14.10 MetaClass和AbstractClass

	- metaclass

	- abstractclass

### 2.15 程序开发规范

- 2.15.1 程序目录结构设计

	- day 20.bmp

- 2.15.2 程序模块划分设计
- 2.15.3 程序日志设计
-  2.15.4 README
- 2.15.5 程序流程图

## 3 网络编程

### 3.1 Socket网络编程

- 3.1.1 Socket原理
- 3.1.2 Socket网络通信开发
- 3.1.3 SocketServer模块源码剖析
- 3.1.4 FTP服务器开发

### 3.2 线程

- 3.2.1 线程操作
- 3.2.2 线程锁
- 3.2.3 信号
- 3.2.4 事件
- 3.2.5 线程池
- 3.2.6 Python的GIL锁内部机制

### 3.3 进程

- 3.3.1 进程操作
- 3.3.2 进程池
- 3.3.3 进程数据共享

### 3.4 协作

- 3.4.1 greenlet
- 3.4.2 Gevent

### 3.5 select、poll、
epoll高性能IO多路复用

- 3.5.1 同步IO
- 3.5.2 异步IO
- 3.5.3 select
- 3.5.4 poll
- 3.5.5 epoll

### 3.6 队列和RabbitMQ

- 3.6.1 RabbitMQ介绍
- 3.6.2 RabbitMQ安装配置
- 3.6.3 RabbitMQ使用-pika模块
- 3.6.4 生产者消费者模型
- 3.6.5 SSH审计服务器开发

### 3.7 Memcached和Redis

- 3.7.1 Memcached介绍
- 3.7.2 Memcached使用
- 3.7.3 Redis介绍
- 3.7.4 Redis安装配置
- 3.7.5 Redis使用-redis模块

### 3.8 MySQL数据库学习

- 3.8.1 数据库原理
- 3.8.2 MySQL安装配置
- 3.8.3 MySQL数据类型
- 3.8.4 MySQL必备之变量和函数
- 3.8.5 MySQL必备之外键、索引和约束
- 3.8.6 MySQL必备之存储过程
- 3.8.7 MySQL必备之视图和触发器
- 3.8.8 MySQL必备之事务和游标
- 3.8.9 数据库设计三大范式
- 3.8.10 SQL语句
- 3.8.11 Python连接数据库
- 3.8.12 数据库连接池

### 3.9 ORM对象关系映射

- 3.9.1 SQLAlchemy介绍
- 3.9.2 SQLAlchemy核心
- 3.9.3 SQLAlchemy ORM

## 4 WEB基础

### 4.1 HTML

- 4.1.3 HTML标签
- 特殊字符

### 4.2 CSS

### 4.3 JavaScript

- 4.3.1 JavaScript基础语法之变量和数据类型
- 4.3.2 JavaScript基础语法之函数
- 4.3.3 JavaScript基础语法之类和对象
- 4.3.4 JavaScript基础语法之原型
- 4.3.5 JavaScript之DOM操作

### 4.4 BootStrap框架

- 4.4.1 BootStrap布局
- 4.4.2 BootStrap应用

### 4.5 jQuery框架

- 4.5.1 jQuery选择器
- 4.5.2 jQuery属性和CSS操作
- 4.5.3 jQuery文档处理
- 4.5.4 jQuery筛选
- 4.5.5 jQuery事件
- 4.5.6 jQuery动画
- 4.5.7 jQuery扩展
- 4.5.8 Ajax原理及jQuery Ajax
- 4.5.9 JSONP原理及jQuery JSONP

### 4.6 CSRF、
Session、Cookie

- 4.6.1 CSRF的由来及实现
- 4.6.2 Session原理及应用
- 4.6.3 Cookie原理及应用

### 4.7 常用插件介绍

- 4.7.1 FontAwesome
- 4.7.2 SweetAlert
- 4.7.3 jQueryUI
- 4.7.4 jQuery Validate

### 4.8 Anjular JS

- 4.8.1 Anjular JS介绍
- 4.8.2 路由
- 4.8.3 指令
- 4.8.4 Service和provider
- 4.8.5 Anjular JS核心原理剖析

## 5 WEB框架

### 5.1 WSGI和自定义开发 WebServer

- 5.1.1 Web框架本质
- 5.1.2 Web请求生命周期
- 5.1.3 WSGI介绍
- 5.1.4 自定义开发Web框架

### 5.2 MVC框架

- 5.2.1 MVC架构的发展史
- 5.2.2 MVC架构组成

### 5.3 Django框架

- 5.3.1 MTV框架介绍
- 5.3.2 Django urls
- 5.3.3 Django模块引擎
- 5.3.4 Django模型绑定
- 5.3.5 Django Form表单
- 5.3.6 Django Session和Cookie
- 5.3.7 Django中间件介绍
- 5.3.8 分页及自定义tag
- 5.3.9 Django缓存
- 5.3.10 XSS和CSRF
- 5.3.11 Django信号
- 5.3.12 Django Admin

### 5.4 Tornado框架

- 5.4.1 Tornado框架介绍
- 5.4.2 Tornado源码剖析

### 5.5 Python其他Web框架

- 5.5.1 Flask框架学习
- 5.5.2 Web.py框架学习
- 5.5.3 Bottle框架学习

### 5.6 其他常用组件

- 5.6.1 highchart动态画图
- 5.6.2 分布式任务队列Celery学习

##  6 项目实战

### 6.1 BSS论坛项目开发

### 6.2 WEB聊天室项目开发

### 6.3 CRM系统开发

### 6.4 购物商城项目开发

### 6.5 分布式监控项目开发

### 6.6 CMDB项目开发

### 6.7 主机管理项目开发

### 6.8 分布式爬虫项目开发

### 6.9 Docker管理平台二次开发

### 6.10 OpenStack二次开发

### 6.11 金融分析项目开发

### 6.12 机器学习项目开发

## 7 算法和设计模式

### 7.1 算法

- 7.1.1 算法定义
- 7.1.2 时间复杂度
- 7.1.3 冒泡排序
- 7.1.4 插入排序
- 7.1.5 快速排序
- 7.1.6 选择排序
- 7.1.7 二叉树及堆排序

### 7.2 设计模式

- 7.2.1 设计模式介绍
- 7.2.2 设计模式分类
- 7.2.3 设计模式六原则
- 7.2.4 常用设计模式介绍

## 8 爬虫

### 8.1 爬虫基础

- 8.1.1 爬虫介绍
- 8.1.2 爬虫原理
- 8.1.3 下载页面-reuqests模块
- 8.1.4 解析页面-
BeautifulSoup模块
- 8.1.5 异步IO模块-
asyncio、aiohttp、
gevent、Twisted、
Tornado

### 8.2 Scrapy框架

- 8.2.1 Command line tool
- 8.2.2 Spiders
- 8.2.3 Selectors
- 8.2.4 Items
- 8.2.5 Item Loaders
- 8.2.6 Scrapy shell
- 8.2.7 Item Pipeline
- 8.2.8 Requests and Responsers
- 8.2.9 Settings
- 8.2.10 Telnet Console

## 9 协作开发

### 9.1 敏捷开发和持续集成

- 9.1.1 软件开发团队工作流程
- 9.1.2 敏捷开发实训
- 9.1.3 Jekins+SaltStack+Docker
实现持续集成开发

### 9.2 代码版本控制系统

- 9.2.1 SVN介绍
- 9.2.2 Git介绍
- 9.2.3 GitHub介绍