---
layout: post
title:  "centos7安装Anaconda(Anaconda3-2020.02-Linux-x86_64)与基本命令使用）"
categories: Python
tags: Aanaconda
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200919163129756.png
---


# 系统环境

我们用Anaconda管理包版本之间的依赖

*此外我还经常用pipenv 和 virtualenv*

```
1 CentOS Linux release 7.7.1908 (Core)
2 Linux version 3.10.0-1062.1.1.el7.x86_64 (mockbuild@kbuilder.bsys.centos.org) (gcc version 4.8.5 20150623 (Red Hat 4.8.5-39) (GCC) ) #1 SMP Fri Sep 13 22:55:44 UTC 2019
```

##  1. 下载


可以去官网下载

 

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-01.png)

 

 

拷贝出来 地址就是:  https://repo.anaconda.com/archive/Anaconda3-2020.02-Linux-x86_64.sh 

```
1 wget https://repo.anaconda.com/archive/Anaconda3-2020.02-Linux-x86_64.sh  
2 
3 # 七牛云
4 http://www.obs.sixmillions.cn/packages/Anaconda3-2020.02-Linux-x86_64.sh
```

 

##  2. 安装


**创建anaconda用户**
**不要用root用户安装,不然,其他普通用户使用不方便**

```
1 useradd anaconda
2 # 改密码
3 passwd anaconda
4 # 默认创建了anacodna用户组
5 id anaconda
```

 

 

**切换到anaconda用户**

```
su anaconda
1 # 进入安装包路径
2 # 运行
3 bash Anaconda3-2020.02-Linux-x86_64.sh 
```

 

 

输入回车

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-02.png)

 

 

 

接受 yes

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-03.png)

 

 

 

选择安装位置默认当前用户home目录下
我们不改变了( /home/anaconda/anaconda3) 反正这个用户就是为了安装anconda创建的
你要改到其他路径,记得要有权限

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-04.png)

 

 

 

运行yes

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-06.png)

 

 

 


\3. 成功

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-07.png)

 

 

 

\4. 环境变量配置
切换到root用户
不配置找不到conda命令.

```
1 vim /etc/bashrc
2 
3 # 添加
4 export PATH=/home/anaconda/anaconda3/bin:$PATH
```

 

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-08.png)

 

 

 

```
1 # 生效
2 source /etc/bashrc
```

 

##  5. 配置国内镜像


 https://mirror.tuna.tsinghua.edu.cn/help/anaconda/ 

切换到anaconda用户登录
先生产配置文件.默认应该是隐藏的

``` bash
conda --config set show_channel_urls yes 
```
因为我用anaconda用户执行的,所以配置文件在 /home/anaconda目录下

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-09.png)

 

 

 

 

```
1 # 编辑
2 vim /home/anaconda/.condarc
```

 


先删除里面的内容

![img](https://raw.githubusercontent.com/weqq2019/weqq2019.github.io/master/img/2020-9-16-12-10.png)

 

 

 

添加



```
channels:
    - defaults
show_channel_urls: true
channel_alias: https://mirrors.tuna.tsinghua.edu.cn/anaconda
default_channels:
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
    conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
```



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2020-9-16-12-11.png)

清除索引缓存，保证用的是镜像站提供的索引

 conda clean -i 

安装完成后重新进一下记得.

 

## 6.改变权限


切换为root用户
将anaconda的home安装路径变为组权限

 chmod -R 775 /home/anaconda 

然后那个普通用户用anaconda 就 加入这个组
虽然普通用户加入这个组能用,但是如果有多个用户的时候,cache还是有问题
最后我直接赋予了777权限

chmod -R 777 /home/anaconda

\6. 测试
 conda -V 



如果显示没有该命令,就重新进一下.

## 7. 错误


安装遇到的错误

```
1 tar: This does not look like a tar archive
2 tar: Exiting with failure status due to previous errors
```

 


安装依赖 bzip2

 yum install -y bzip2 

 

## 8. 命令

　　**基本命令**



```
 1 # 版本
 2 conda --version
 3 conda -V
 4 
 5 # 创建一个环境
 6 conda create --name tensorflow1_env python=3.6
 7 # --name可以简写成-n
 8 conda create -n tensorflow1_env python=3.6
 9 
10 # 显示环境列表
11 conda env list 
12 conda info --env
13 #简写成-e
14 conda info -e
15 
16 # 查看tensorflow1_env 该环境安装哪些依赖
17 conda list -n tensorflow1_env 
18 
19 # 激活该环境
20 conda activate tensorflow1_env 
21 
22 # 在激活的环境里面查找tensorflow安装包
23 conda search tensorflow
24 
25 # 安装一个版本
26 conda install tensorflow==1.14.0
27 
28 # 更新一个包
29 conda update numpy
30 
31 # 退出环境
32 conda deactivate
33 
34 # 删除环境(千万不要乱删除  )
35 conda remove tensorflow1_env
36 或者  
37 conda remove -n tensorflow1_env --all
38 conda remove --name  tensorflow1_env --all
39 
40 # 显示总的依赖list
41 conda list
```

##  

## **升级**

**Anaconda需要先升级conda**

```
1 conda update conda #基本升级
2 conda update anaconda #大的升级
3 conda update anaconda-navigator //update最新版本的anaconda-navigator
4 
5 conda update -n xxx conda #update某个环境的到最新版本的conda
```

 

 


**卸载anaconda**

删除

 rm -rf /home/anaconda/anaconda3/ 

注释掉环境变量