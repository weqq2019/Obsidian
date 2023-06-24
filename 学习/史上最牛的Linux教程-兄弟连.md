---
layout: post
title: 史上最牛的Linux教程-兄弟连
categories: [Linux,Linux]
tags: Linux
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924200319608.png
---

![image-20200924200319608](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924200319608.png)

# 1. Linux 系统简介

## 1.1.1 UNIX 发展历史和发行版本

> UNIX 发展历史

### 1. UNIX 与 Linux发展史

​	( 1 ) 1965年,美国麻省理工学院 ( MIT )、 通用电气公司 ( GE ) 及 AT&T 的贝尔实验室联合开发 `Multics` 工程计划 , 其目标是开发一种交互式的具有多道程序处理能力的分时操作系统 , 但因 `Multics` 追求的目标过于宠大复杂 , 项目进度远远落后计划 , 最后贝尔实验室宣布退出 .

​	( 2 ) 1969年 , 美国贝尔实验室的 肯・汤普森在 DEC PDP-7 机器上开发出了 `UNIX` 系统

​	( 3 ) 1971年 , 肯・汤普森的同事丹尼斯・里奇发明了 `C 语言` : 1973年 , `UNIX` 系统的绝大部分源代码用`C语言`重写 , 这为提高 `UNIX` 系统的可移值性打下基础 .

![image-20200924202000512](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924202000512.png)

肯・汤普森

![image-20200924202112834](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924202112834.png)

丹尼斯・里奇

> UNIX 主要发行版本

| 操作系统 |                公司                |                  硬件平台                  |
| :------: | :--------------------------------: | :----------------------------------------: |
|   AIX    |                IBM                 |                  PowerPC                   |
|  HP-UX   |                 HP                 |                  PA-RISC                   |
| Solaris  |                Sun                 |                   SPARC                    |
|  Linux   | Red Hat Liunx、Ubuntu Linux ...... | IA ( Intel 、 AMD 、 Cyrix 、 RISE ......) |

## 1.1.2 UNIX 发展历史和发行版本

>  `Linux` 发展历史

`Linux`系统诞生于1991年,由芬兰大学生李纳斯( Linus Torvalds ) 和后来陆续加入的众多爱好者共同开发完成.

`Linux` 是开源软件 ,  源代码开放的 `UNIX` .

![image-20200924203718772](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924203718772.png)

> `Linux` 内核版本

`Linux` 内核官网:www.kernel.org

内核版本说明:2.6.18

目前最新的内核版本 5.8.11

> `Linux` 主要发行版本

![image-20200924204341935](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924204341935.png)





## 1.2 开源应用领域

![image-20200924204643540](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924204643540.png)

> 开源软件

- **使用的自由**

  ​	绝大多数开源软件免费

- **研究的自由**

  ​	可以获得软件源代码

- **散布及改良的自由**

  ​	可以自由传播、改良甚至销售

> 支撑互联网的开源技术

![image-20200924205133382](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924205133382.png)



## 1.3 Linux 应用领域

### 1.3.1 基于`Linux`的企业服务器

> www.netcraft.com 查看站点服务器使用的是什么操作系统

![image-20200924205614157](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924205614157.png)

![image-20200924205954690](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924205954690.png)

【不知道在哪里看,谁知道的告诉我 谢谢】



### 1.3.2 嵌入式应用

1. ​	手机、平板电脑

![image-20200924210154040](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924210154040.png)

2. 其他嵌入式应用
   - 智能家电:机顶盒  、游戏机 、数码相机等
   - 智能卡系统
   - 航空系统
   - 银行系统
   - 卡拉 OK 点歌系统
   - ...... 



### 1.3.3 `Linux`在电影娱乐业

![image-20200924210606616](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924210606616.png)



## 1.4. Linux  学习方法

![image-20200924210831581](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924210831581.png)

> 解决问题的智慧

- 帮助
- 示例
- 文档
- 查找

![image-20200924211529943](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924211529943.png)

> 忘掉WIndows思维方式

**学习方法**

`计划`

`专注`

`坚持`

`练习`

# 2. `Linux`系统安装

## 2.1 `Vmware`虚拟机安装与使用

### 2.1.1 `Vmware`简介

​	`VMware`是一个虚拟 PC 的软件,可以在现有的操作系统上虚拟出一个新的硬件环境,相当于模拟出一台新的PC,以此来实现在一台机器上真正同时运行两个独立的操作系统.

​	`Vmware`官方网站 http://www.vmware.com

​	`VMware`主要特点:

- 不需要分区或重新开机就能在同一台PC上使用两种以上的操作系统
- 本机系统可以与虚拟机系统网络通信
- 可以设定并且随时修改虚拟机操作系统的硬件环境    

### 2.1.2 建议的`VMware`配置

- ​	CPU : 建议主频为1GHZ以上
-    内存 : 建议1GB以上
-    硬盘 : 建议分区空闲空间8GB以上



> VMware-Workstation-Lite-15.5.6-16341506精简官方中文安装注册版 ( 可以找我要)

![image-20200924215601624](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924215601624.png)

![image-20200924220352563](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924220352563.png)

![image-20200924220401103](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924220401103.png)

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924221053053.png)

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924221105911.png)

![image-20200924220512263](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924220512263.png)

![image-20200924220541407](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924220541407.png)

![image-20200924220652132](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924220652132.png)



![image-20200924221437627](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924221437627.png)



![image-20200924231639130](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924231639130.png)

## 2.2 系统分区

### 2.2.1 磁盘分区

磁盘分区是使用分区编辑器 ( partition editor ) 在磁盘上划分几个逻辑部分.碟片一旦划分成数个分区 ( Partition ),不同类的目录与文件可以储存进不同的分区.

> 分区类型

- 主分式 : 最多只能有4个
- 扩展分区:
  - 最多只能有1个.
  - 主分区加扩展分区最多4个.
  - 不能写入数据 , 只能包含逻辑分区
- 逻辑分区

### 2.2.2 格式化

格式化 ( 高级格式化 ) 又称逻辑格式化 , 它是指根据用户选定的文件系统( 如 FAT16 、FAT32 、NTFS 、EXT2 、EXT3 、EXT4 等 ) ,在磁盘的特定区域写入特定数据,在分区中划出一片用于存放文件分配表、目录表等用于文件管理的磁盘空间.

### 2.2.3 硬件设备文件名

| 硬件                   | 设备文件名                   |
| ---------------------- | ---------------------------- |
| IDE硬盘                | / dev / hd [ a - d]          |
| SCSI / SATA / USB 硬盘 | / dev / sd [ a - p]          |
| 光驱                   | / dev / cdram 或 / dev / sr0 |
| 软盘                   | / dev / fd [ 0-1 ]           |
| 打印机 ( 25 针 )       | / dev / lp [ 0 -2 ]          |
| 打印机 ( USB )         | / dev / usb / lp [ 0 - 15]   |
| 鼠标                   | / dev / mouse                |

> 分区设备文件名

- 设备文件名
  - / dev / hda1 ( IDE 硬盘接口 )
  - / dev / sda1 ( SCSI 硬盘接口 、 SATA 硬盘接口 )

![image-20200924234417827](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924234417827.png)

![image-20200924234457289](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924234457289.png)



![image-20200924234542362](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924234542362.png)



### 2.3.4 挂载

- 必须分区
  - `/`( 根分区 )
  - `swap`分区 ( 交换分区 , 内存 2 倍 , 不超过 2 GB)
- 推荐分区
  - ​	`/boot `( 启动分区 , 200MB)

![image-20200924235710211](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924235710211.png)

扩展

![image-20200924235851202](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200924235851202.png)

> **总结**

- 分区 : 把大硬盘分为小的逻辑分区
- 格式化 : 写入文件系统
- 分区设备文件名 : 给每个分区定义设备文件名
- 挂载 : 给每个分区分配挂载点



## 2.3 `Linux` 系统安装

![image-20200925010554974](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925010554974.png)

选第1个

### 2.3.1 安装欢迎界面

- Install or upgrade an existing system # 安装或升级现有系统
- Intstall system with basic video driver # 安装过程采用基本的显卡驱动
- Rescue installed system # 进入系统修复模式
- boot from local drive # 退出安装从硬盘启动
- Memory test #存储介质检测

![image-20200925011341710](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925011341710.png)

![image-20200925011415220](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925011415220.png)

![image-20200925011539378](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925011539378.png)



![image-20200925011623699](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925011623699.png)



![image-20200925011805031](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925011805031.png)

![image-20200925012358665](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925012358665.png)

###  2.3.2 密码原则

- 复杂性
  - 八位字符以上,大小写字母、数字、符号
  - 不能是英文单词
  - 不能是和用户相关的内容
- 易记忆性
- 时效性

![image-20200925012543232](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925012543232.png)

![image-20200925012615369](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925012615369.png)

![image-20200925013420053](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925013420053.png)

![image-20200925013434377](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925013434377.png)

![image-20200925013515936](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925013515936.png)



![image-20200925013610385](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925013610385.png)



![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925014536081.png)

###  2.3.3 软件包选择

- Desktop # 桌面
- Minimal Desktop # 最小化桌面
- Minimal # 最小化
- Basic Server #基本服务器
- Database Server # 数据库服务器
- Web Server #网页服务器
- Virtual Host #虚拟主机
- software development workstation #软件开发工作站

![image-20200925014602135](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925014602135.png)



![image-20200925015203001](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925015203001.png)

![image-20200925015543918](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925015543918.png)



![image-20200925015627918](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925015627918.png)



![image-20200925015725874](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925015725874.png)



###  2.3.4 安装日志

- /root/install.log # 存储了安装在系统中的软件包及其版本信息
- /root/install.log.syslog # 储存了安装过程中留下的事件记录
- /root/anaconda-ks.cfg # 以Kickstart配置文件的格式记录安装过程中设置的选项信息

## 2.4 远程登录管理工具

![image-20200925022011960](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925022011960.png)

![image-20200925021944014](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925021944014.png)

 ![image-20200925021500818](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925021500818.png)

![image-20200925021520487](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925021520487.png)

![image-20200925022028548](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925022028548.png)

如果得到这样的一个ping请求包请求应答包,那么就证明了我们网络设置已经成功了,现在就可以直接用远程工具来连接,



![image-20200925022443600](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925022443600.png)



![image-20200925023535801](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925023535801.png)

![image-20200925023601385](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925023601385.png)

> 总结

设置 `Linux`的 IP 地址

```shell
 ifconfig eth0 192.168.0.156
```

![image-20200925025419486](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925025419486.png)



![image-20200925025453857](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925025453857.png)

顺便改

[`Xshell`主题]: http://kuailell.com/2020/09/25/%E6%8E%A8%E8%8D%90%E4%B8%80%E4%B8%AA%E6%AF%94%E8%BE%83%E9%AA%9A%E6%B0%94%E7%9A%84Xshell%E9%85%8D%E8%89%B2%E6%96%B9%E6%A1%88%20%E4%B8%AA%E4%BA%BA%E5%BE%88%E6%98%AF%E5%96%9C%E6%AC%A2/

 ,

![image-20200925031545735](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925031545735.png)



![image-20200925032118965](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925032118965.png)

> 远程登录管理工具
> ```Xshell```是一个强大的安全终端模拟软件，它支持SSH1, SSH2, 以及Microsoft Windows 平台的TELNET 协议
>
> ```Xftp``` 是一个功能强大的SFTP、FTP 文件传输软件。使用了 *Xftp* 以后，MS Windows 用户能安全地在 UNIX/Linux 和 Windows PC 之间传输文件。

#  3. 给初学者的建议

## 3.1 注意事项

### 3.1.1 学习 ```Linux```的注意事项

- ``` Linux ``` 严格区分大小写

- ``` Linux``` 中所有内容以文件形式保存,包括硬件

  - 硬盘文件是/dev/sd[a-p]
  - 光盘文件是/dev/str0等

- ```Linux```不靠扩展名区分文件类型

  - 压缩包 

    ```  shell
    "*.gz" , "*.bz2" , "*.tar.bz2" , "*.tgz" .....
    ```

  - 二进制软件包

    ```shell
    ".rpm"
    ```

  - 网页文件

    ```shell
    "*.html" , "*.php"
    ```

  - 脚本文件

    ```shell
    "*.sh"
    ```

    

  - 配置文件

    ```shell
    "*.conf"
    ```

- ``` Linux``` 所有的存储设备都必须挂载之后用户才能使用,包括硬盘 、 U盘和光盘

- ```Windows``` 下的程序不能直接在```Linux```中安装和运行

### 3.1.2 服务器管理和维护建议

#### 	3.1.2.1 ```Linux``` 各目录的作用

| 目录名       | 目录作用                                                     |
| ------------ | ------------------------------------------------------------ |
| /bin/        | 存放系统命令的目录,普通用户和超级用户都可以执行.<br />不过放在/bin下的命令在单用户模式下也可以执行 |
| /sbin/       | 保存和系统环境设置相关的命令,只有超级用户可以使用这些命令进行系统环境设置,但是有些命令可以允许普遍用户查看. |
| /usr/bin/    | 存放系统命令的目录,普通用户和超级用户都可以执行.这些命令和系统启动无关,在单用户模式下不能执行. |
| /usr/sbin/   | 存放根文件系统不必要的系统管理命令,例如多数服务程序.只有超级用户可以使用.大家其实可以注意到```Linux```的系统,在所有“ sbin ” 目录中保存的命令只有超级用户可以使用,” bin ” 目录中保存的命令所有用户都可以使用 |
| /boot/       | 系统启动目录,保存系统启动相关的文件 , 如内核文件和启动引导程序 ( grub ) 文件等 |
| /dev/        | 设备文件保存位置 . 我们已经说过 ```Linux```中所有内容以文件形式保存 , 包括硬件 . 那么这个目录就是用来保存所有硬件设备文件的. |
| /etc/        | 配置文件保存位置. 系统内所有采用默认安装方式 ( rpm 安装 ) 的服务的配置文件全部都保存在这个目录当中 , 如用户帐户和密码 , 服务的启动脚本 , 常用服务的配置文件等 |
| /home/       | 普遍用户的家目录 . 建立每个用户时 , 每个用户要有一个默认登录位置 , 这个位置就是这个用户的家目录 , 所有普遍用户的家目录就在 /home 下建立一个和用户名相同的目录 . 如用户 user1 的家目录就是 /home/user1 |
| /lib/        | 系统调用的函数库保存位置 |
| /lost+found/ | 当系统意外崩溃或机器意外关机 , 而产生一些文件碎片放在这里 . 当系统启动的过程fsck工具会检查这里 , 并修复已经损坏的文件系统 . 这个目录只在每个分区中出现 . 例如 /lost+found 就是根分区的备份恢复目录 , /boot/lost+found 就是 /boot 分区的备份恢复目录 |
| /media       | 挂载目录 . 系统建议是用来挂载媒体设备的 . 例如软盘和光盘 |
| /mnt/ | 挂载目录 . 早期```Linux```中只有这一个挂载目录,并没有细分 . 现在这个目录系统建议挂载额外设备 , 如U盘 , 移动硬盘和其他操作系统的分区 |
| /misc/ | 挂载目录 . 系统建议用来挂载NFS服务的共享目录 . 我们在刚刚已经解释了挂载,童鞋们应该知道只要是一个已经建立的空目录就可以作为挂载点 . 那么系统虽然准备了三个默认挂载目录/media、/mnt、/misc , 但是到底在哪个目录中挂载什么设备都可以由管理员自己决定 . 例如 超哥接触```Linux```的时候,默认挂载目录只是 /mnt 一个,所以养成了 在/mnt 下建立不同目录挂载不同设备的习惯 . 如 /mnt/cdrom 挂载光盘 , /mnt/usb挂载U盘 , 这都是可以的. |
| /opt/ | 第三方安装的软件保存位置 . 这个目录就是放置和安装其他软件的位置 , 我手工安装的源码包软件都可以安装到这个目录当中 . 不过我还是更加习惯把软件放置到/usr/local/目录当中  ,  也就是说/usr/local/目录也可以用来安装软件 |
| /proc/ | 虚拟文件系统 , 该目录中的数据并不保存到硬盘当中,而是保存到内存当中 , 主要保存系统的内核 , 进程 , 外部设备状态和网络状态灯 . 如/proc/cpuinfo是保存CPU信息的 , /proc/devices 是保存设备驱动的列表的 , /proc/filesystems 是保存文件系统列表的 , /proc/net/ 是保存网络协议信息的 . |
| /sysy/ | 虚拟文件系统 . 和 /proc 目录相似 . 都是保存在内存当中的 , 主要是保存于内核相关信息的 |
| /root/ | 超级用户的家目录 . 普遍用户家在 “ /home ”下 , 超级用于家目录直接“/”下 |
| /srv/ | 服务数据目录 . 一些系统服务启动之后 , 可以在这个目录中保存所需要的数据 . |
| /tmp/ | 临时目录 . 系统存放临时文件的目录 , 该目录下所有用户都可以访问和写入 . 我们建议此目录中不能保存重要数据 . 最好每次开机都把该目录清空 . |
| /usr/ | 系统软件资源目录 . 注意usr 不是user的缩写 , 而是 “ Unix software Resource” 的缩写 , 所以不是存放用户数据 , 而是存放系统软件资源的目录 . 系统中安装的软件大多数保存在这里 , 所以除了 /usr/bin/ 和/usr/sbin/这两个目录 ,我在介绍几个 /usr/下的二级目录 . |
| /var/ | 动态数据保存位置 . 主要保存缓存 、 日志以及软件运行所产生的文件 . |

	#### 3.1.2.2 服务器注意事项

- 远程服务器不允许关机 , 只能重启
- 重启时应该关闭服务

> 

- 不要在服务器访问高峰运行高负载命令
- 远程配置防火墙时不要把自己踢出服务器

> 

- 指定合理的密码规范并定期更新
- 合理分配权限
- 定期备份重要数据和日志

# 4. ```Linux``` 常用命令

## 4.1 文件处理命令

### 4.1.1 命令格式和目录处理命令 `` ls ``

> 命令格式

命令格式 : 命令 [-选项] [参数]

​			  例 : 

 ``` shell
ls -la /etc
 ```

说明: 

1. 个别命令使用不遵循此格式

2. 当有多个选项时,可以写在一起

3. 简化选项与完整选项

   -a  等于 --all



> 目录处理命令: ```ls```

命令名称 :  ```ls```

命令英文原意 : list

命令所在路径 : /bin/```ls```

执行权限 : 所有用户

功能描述 : 显示目录文件

语法 :  选项 [-ald] [文件或目录]

​					-a	显示所有文件,包括隐藏文件

​					-l	详细信息显示

​					-d	查看目录属性

```拓展```

ll 等于 ls -l

ls -a -l -d -h -i 

-  -h, --human-readable		与-l 一起，以易于阅读的格式输出文件大小
-  -i, --inode			显示每个文件的inode 号



![image-20200925054747106](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925054747106.png)

![image-20200925054818981](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925054818981.png)

> -rw-r--r--

- -rw-r--r--

  - -文件类型 ( - 二进制文件 d目录 l 软链接文件)

  - rw- r-- r-- 

    u	g	o

    u所有者	g所属组	o其他人

    r读	w写	x执行

### 4.1.2 目录处理命令 ```mkdir``` ```cd``` ```pwd``` ```rmdir``` `cp` ```mv``` ```rm``` `du`

> 目录处理命令 : ``` mkdir``` 

命令名称 : ``` mkdir ```

命令英文原意 : `m`a`k`e `dir`ectories

命令所在路径 : /bin/```mkdir```

执行权限 : 所有用户

语法:	mkdir -p [ 目录名]

功能描述 : 创建新目录

​						-p 递归创建

范例: 

``` shell
$ mkdir -p /tmp/japan/boduo
```

```shell
$ mkdir /tmp/japan/longze /tmp/Janpan/cangjing
```

> 目录处理命令 : ```cd```

命令名称 : ```cd```

命令英文原意 : `c`hange `d`irectory

命令所在路径 : shell内置命令

执行权限 : 所有用户

语法 : cd [目录]

功能描述 : 切换目录

范例 : 

```shell
$ cd /tmp/Japan/boduo    #切换到指定目录
```

```shell
$ cd .. 	#回到上一级目录
```

> 目录处理命令 : ```pwd ```

命令名称 : ` pwd `

命令英文原意 : `p`rint `w`orking `d`irectory

命令所在路径  : /bin/`pwd`

执行权限 : 所有用户

语法 : pwd

功能描述 : 显示当前目录

范例:

```shell
$ pwd
```

结果:/tmp/Janan

> 文件处理命令 : ```rmdir```

命令名称 : `rmdir`

命令英文原意 : `r`e`m`ove empty directory

命令所在路径 : /bin/`rmdir`

执行权限 : 所有用户

语法 : `rmdir` [目录]

功能描述 : 删除空目录

范例 : 

```shell
$ rmdir /tmp/Japan/boduo
```

> 目录处理命令 :` cp`

命令名称 : `cp`

命令英文原意 : `c`o`p`y

命令所在路径 : /bin/`cp`

执行权限 : 所有用户

语法 : `cp`	-rp 	[原文件或目录] [目标目录]

​							-r	复制目录

​							-p	保留文件属性

功能描述 :复制文件或目录 

范例 : 

```shell
$ cp -r /tmp/Japan/cangjing /root
```

​	将目录/tmp/Janan/cangjian复制到目录/root下

```shell
$ cp -rp /tmp/Japan/boduo /tmp/Japan/longze /root
```

​	将/tmp/Japan目录下的boduo和longze目录复制到/root下,保持目录属性

> 目录处理命令 : `mv`

命令名称 : `mv`

命令英文原意 : `m`o`v`e

命令所在路径 : /bin/`mv`

执行权限 : 所有用户

语法 : `mv ` [原文件或目录] [目标目录]

功能描述 : 剪切文件 、 改名

> 目录处理命令 : `rm`

命令名称 : `rm`

命令英文原意 : `r`e`m`ove

命令所在路径  : /bin/`rm`

执行权限:所有用户

语法  : `rm` -rf [ 文件或目录]

​						-r 删除目录

​						-f 强制执行

功能描述 : 删除文件

### 4.1.3 文件处理命令 `touch` `cat` `more` `less` `head` `tail`

> 文件处理命令 : `touch`

命令名称 : `touch`

命令所在路径 : /bin/`touch`

执行权限 : 所有用户

语法 : touch [文件名]

功能描述 : 创建空文件

范例 : 

```shell
$ touch Janpanlovestory.list
```

> 文件处理命令 :` cat`

命令名称 : cat

命令所在路径 : /bin/`cat`

执行权限 : 所有用户

语法  : `cat`[文件名]

功能描述 : 显示文件内容

​						-n 显示行号

范例 : 

``` shell
$ cat /etc/issue
```

``` shell
$ cat -n /etc/services
```



>文件处理命令 : `more`

命令名称 : `more`

命令所在路径 : /bin/`more`

执行权限 : 所有用户

语法 : `more` [文件名]

​				(空格)或f	翻页

​				(Enter)		换行

​				q或Q			退出

功能描述 : 分页显示文件内容

范例 : 

```shell
$ more /etc/services
```



> 文件处理命令 : `less`

命令名称 : `less`

命令所在路径 : /usr/bin/`less`

执行权限 : 所有用户

语法 : `less`[文件名]

功能描述 : 分页显示文件内容 ( 可向上翻页)

范例 : 

```shell
$ less /etc/services
```



> 文件处理命令 : `head`

命令名称 : ` head`

命令所在路径 : /usr/bin/`head`

执行权限 : 所有用户

语法 : `head `[文件名]

功能描述 : 显示文件前面几行

​						-n 指定行数

范例 :

```shell
$ head -n 20 /etc/services
```



> 文件处理命令 : ` tail `

命令名称 : `tail `

命令所在路径 : /usr/bin/`tail`

执行权限 : 所有用户

语法 : `tail`[文件名]

功能描述 : 显示文件后面几行

​						-n 指定行数

​						-f 动态显示文件未尾内容

范例 : 

```shell
$ tail -n 18 /etc/services
```

![image-20200925233451343](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200925233451343.png)

### 4.1.4 链接命令 `ln`

> 文件处理命令 : ` ln`

命令名称 : ln

命令英文原意 : `l`i`n`k

命令所在路径  : /bin/`ln`

执行权限 : 所有用户

语法 : `ln `	-s	[原文件] [目标文件]

​						  -s	创建软链接

功能描述 : 生成链接文件

范例:

```shell
$ ln -s /etc/issue /tmp/issue.soft
```

​	创建文件/etc/issue的软链接/tmp/issue.soft

```shell
$ ln /etc/issue /tmp/issue.hard
```

​	创建文件/etc/issue的硬链接/tmp/issue.hard

软链接特征 : 类似Windows快捷方式

1. lrwxrwxrwx 	l 软链接
2. 文件大小 -只是符号链接
3. /tmp/issue.soft -> /etc/issue

硬链接特征 :

1、拷贝 cp -p +同步更新

```shell
echo "www.lampbrother.net" >> /etc/issue
```

2、 通过i节点识别

3、 不能跨分区

4、 不能针对目录使用

> du   报告磁盘空间使用情况

## 4.2 权限管理命令

### 4.2.1 权限管理命令 `chomd`

> 权限管理命令 : chmod

命令名称 : chmod

命令英文原意 : `ch`anage the permissions `mod`e of a file

命令所在路径 : /bin/`chmod`

执行权限 : 所有用户

语法 : `chmod` [ { ugoa } { +-= } { rwx } ] [ 文件或目录 ]

​								[mode =421 ] [  文件 或 目录 ]

​								-R 递归修改

功能描述 : 改变文件或目录权限

> 权限的数字表示

r --- 4

w ---- 2

x ---- 1

rwxrw-r--

7 6 4

范例 : 

```shell
$ chmod g+w testfile
```

​	赋予文件 testfile 所属组写权限

```shell
$ chmod -R 777 testdir
```

​	修改目录 testfile 及其目录下文件为所有用户具有全部权限

> 文件目录权限总结

| 代表字符 | 权限     |   对文件的含义   | 对目录的含义               |
| :------: | -------- | :--------------: | -------------------------- |
|    r     | 读权限   | 可以查看文件内容 | 可以列出目录中的内容       |
|    w     | 写权限   |   可以修改文件   | 可以在目录中创建、删除文件 |
|    x     | 执行权限 |   可以执行文件   | 可以进入目录               |

file :

​		r : cat/more/head/tail/less

​		w : vim

​		x : script command

directory : 

​		r : ls

​		w : touch/mkdir/rmdir/rm

​		x : cd 

chmod + - =

​				r=4 w=2 x=1



### 4.2.2 其他权限管理命令 `chown` `chgrp` `umask`

> 权限管理命令 :` chown`

命令名称 : `chown`

命令英文原意 : `ch`ange file `own`ership

命令所在路径 : 所有用户

语法 : `chown` [ 用户 ] [ 文件或目录]

功能描述 : 改变文件或目录的所有者

范例 : 

```shell
$ chown shenchao weqq02
```

​			改变文件fengjie的所有者为weqq02



>  权限管理命令 `chgrp`

命令名称 : chgrp

命令英文原意 : `ch`ange file `gr`ou`p` ownership

命令所在路径 : /bin/`chgrp`

执行权限 : 所有用户

语法 : `chgrp` [ 用户组 ] [ 文件或目录 ]

功能描述 : 改变文件或目录的所属组

范例 : 

```shell
$ chgrp lampbrother fengjie
```

​	改变文件fengjie的所属组为lampbrother



> 权限管理命令 : `umask`

命令名称 : `umask`

命令英文原意 : the `u`ser file-creation `mask`

命令所在路径 : Shell内置命令

语法 : `umask`[ -S ]

​				-S 以 rwx 形式显示新建文件缺省权限

功能描述 : 显示 、 设置文件的缺省权限

范例 : 

```shell
$ umask -S
```

```shell
$ umask
```

### 总结

0022

0		特殊权限

022	--- -w--w-	



777	rwx rwx rwx

022 	--- -w- -w-

--------------------------

755	rwx r-x r-x	目录

​			rw- r-- r-- 	文件



777	rwx rwx rwx

077	---   rwx rwx 

----------------------------------

700	rwx --- --- 	目录

​			rw --- ---		文件

## 4.3 文件搜索命令 `find` `locate` `which` `whereis` `grep`

### 4.3.1 文件搜索命令`find`

> 文件搜索命令 : `find`

命令名称 : `find`

命令名称 : /bin/`find`

执行权限 : 所有用户

语法 : find [ 搜索范围 ] [ 匹配条件 ]

功能描述 : 文件搜索

范例 : 

```shell
$ find /etc -name init
```

​	-iname 不区分大小写

```shell
$ find / -size +204800
```

​	在根目录下查找大于100MB的文件

​	+n 大于 -n 小于 n等于

```shell
$ find /home -user shenchao
```

​	在根目录下查找所有者为shemchao的文件

​	-group 根据所属组查找

```shell
$ find /etc -cmin -5
```

​	在/etc下查找5分钟内被修改过属性的文件和目录

​	-amin 访问时间 access

​	-cmin 文件属性 change

​	-mmin 文件内容 modify

``` shell
$ find /etc -size +163840 -a -size -204800
```

​	在/etc 下查找大于80MB小于100MB文件

​	-a 两个条件同时满足

​	-o 两个条件满足任意一个即可

```shell
$ find /etc -name inittab -exec ls -l {} \;
```

​	在/etc下查找inittab文件并显示其详细信息

​	-exec/-ok 命令 {} \; 对搜索结果执行操作

> -type 根据文件类型查找

​				f 文件 d 目录 l 软链接文件

> -inum 根据i节点查找

总结:

find -name -iname * ?   -size +n -n =n -user -group -amin -cmin -mmin -type f d l  -inum -a -o  -exec/-ok {} \;

### 4.3.2 其他搜索命令`locate` `which` `wheris` `grep`

> 文件搜索命令 :` locate`

命令名称 :  `locate`

命令所在路径 : /usr/bin/`locate`

功能描述 : 在文件资料库中查找文件

范例 : 

```shell
$ locate inittab
```

有一个他相对应的命令叫 `updatedb` 这个时候他会去更新文件资料库,更新以后我们再来做一个查找. 

>文件搜索命令 : `which`

命令名称 : `which`

命令所在路径 : /usr/bin/`which`

执行权限 : 所有用户

语法 : `which` 命令

功能描述 : 搜索命令所在目录及别名信息

范例 : 

```shell
$ which ls
```

> 文件搜索命令 : `whereis`

命令名称 : `whereis`

命令所在路径 : /usr/bin/`whereis`

执行权限 : 所有用户

语法 : whereis [ 命令名称 ]

功能描述 : 搜索命令所在目录及帮助文档路径

范例 : 

```shell
$ whereis ls
```

> 文件搜索命令 : `grep`

命令名称 : `grep`

命令所在路径 : /bin/`grep`

执行权限 : 所有用户

语法 :  `grep` -iv [ 指定字串] [ 文件 ]

功能描述 : 在文件中搜寻字串匹配的行并输出 

​						-i	不区分大小写

​						-v	排除指定字串

范例 : 

```shell
# grep mysql /root/install.log
```

### 总结

find locate -i  updatedb  which whereis grep -i -v 

## 4.4 帮助命令 `man`

> 帮助命令 : `man` `whatis` `apropos` `help`

命令名称 : `man`

命令英文原意 : `man`ual

命令所在路径 :/usr/bin/`man`

执行权限 : 所有用户

语法 : `man` [ 命令或配置文件 ]

功能描述 : 获得帮助信息

范例 : 

```shell
$ man ls
```

​	查看ls命令的帮助信息

```shell
$ man services
```

​	查看配置文件services的帮助信息

1 命令的帮助		5 配置文件的帮助

> `whatis `命令是用于查询一个命令执行什么功能，并将查询结果打印到终端上。 

范例 : 

```shell
whatis ls
whatis ifconfig
```

> `apropos` - 在 whatis 数据库中查找字符串

范例

```shell
apropos services
```

`whatis` 查看命令简短的信息				`apropos` 查看配置文件的简短信息



> 帮助命令: `help`

命令名称 : `help`

命令所在路径 : Shell内置命令

执行权限 : 所有用户

语法 : `help`命令

功能描述 : 获得 Shell 内置命令的帮助信息

范例 : 

```shell
$ help umask
```

​	查看umask命令的帮助信息

### 总结

`man` 命令或配置文件		命令	NAME 作用			/选项

​													   配置文件	NAME 存放信息		文件格式

`whatis`	命令

`apropos`	配置文件

命令 --help

info

date 	man date

help 

## 4.5 用户管理命令

>  用户管理命令 :` useradd`

命令名称 : useradd

命令所在路径  : /usr/sbin/`useradd`

执行权限 : root

语法 : useradd 用户名

功能描述 : 添加新用户

范例 :

```shell
$ useradd yangmi
```

> 用户管理命令 : `passwd`

命令名称 :` passwd`

命令所在路径 : /usr/bin/`passwd`

执行权限 : 所有用户

语法 : passwd 用户名

功能描述 : 设置用户密码

范例 : 

```shell
$ passwd yangmi
```

> 用户管理命令 : `who`

命令名称 : `who`

命令所在路径 : /usr/bin/`who`

执行权限 : 所有用户

语法 : who

功能描述 : 查看登录用户信息

范例 : 

```shell
$ who
```

登录用户名	登录终端	tty本地终端	pts远程终端	登录时间	IP地址

> 用户管理命令 :` w`

命令名称 : `w`

命令所在的路径 : /usr/bin/`w`

执行权限 : 所有用户

语法 : `w`

功能描述 : 查看登录用户详细信息

范例 : 

```shell
$ w
```

### 总结

useradd passwd who w

## 4.6 压缩解压命令

> 压缩解压命令 : `gzip`

命令名称 : `gzip`

命令英文原意 : `G`NU `zip`

命令所在路径 : /bin/`gzip`

语法 : `gzip` [  文件 ]

功能描述 : 压缩文件

压缩后文件格式 : .gz

> 压缩解压命令 : `gunzip`

命令名称 :` gunzip`

命令英文原意 : `G`NU `zip`

命令所在路径 : /bin/`gunzip`

执行权限 : 所有用户

语法 : `gunzip` [ 压缩文件]

功能描述 : 解压缩 .gz 的压缩文件

范例 : 

```shell
$ gunzip boduo.gz
```

> 压缩解压命令 : `tar`

命令名称 : `tar`

命令所在路径 : /bin/`tar`

执行权限 : 所有用户

语法 : `tar` 选项 [ -zcf ] [压缩后文件名] [目录]

​							-c 	打包

​							-v 	显示详细信息

​							-f 	指定文件名

​							-z 	打包同时压缩

功能描述 : 打包目录

压缩后文件格式 : .tar.gz

范例 : 

```shell
$ tar -zcf Japan.tar.gz Japan
```

	>`tar`命令解压缩语法 :

​				-x 	解包

​				-v 	显示详细信息

​				-f 	指定解压文件

​				-z 	解压缩

> 压缩解压命令 :  `zip`

命令名称 :` zip`

命令所在路径 : /usr/bin/`zip`

执行权限 : 所有用户

语法 : 

​	`zip`	选项[-r]	[压缩后文件名]	[文件或目录]

​					-r	压缩目录

功能描述 : 压缩文件或目录

压缩后文件格式 : 	.zip

>压缩解压集合: unzip

命令名称 :` unzip`

命令所在路径 : /usr/bin/`unzip`

执行权限 : 所有用户

语法 : 

​	`unzip`	选项[-r]	[压缩后文件名]	[文件或目录]

​					-r	压缩目录

功能描述 : 解压.zip的压缩文件

范例 :

```shell
$ unzip test.zip
```

> 压缩解压命令 :` bzip2`

命令名称 : `bzip2`

命令所在路径 : /usr/bin/`bzip2`

执行权限 : 所有用户

语法 : `bzip2` 	选项[-k] [文件]

​									-k		产生压缩文件后保留原文件

功能描述 : 压缩文件

压缩后文件格式 : .bz2

范例 : 

```shell
$ bzip2 -k boduo
```

```shell
$ bzip2 -cjf Japan.tar.bz2 Japan
```

> 压缩解压命令 : `bunzip2`

命令名称:	`bunzip2`

命令所在路径 : /usr/bin/`bunzip2`

执行权限 : 所有用户

语法 : `bunzip2`	选项 [=k] [压缩文件]

​												     -k 	解压缩后保留原文件

功能描述 : 解压缩

范例 : 

```shell
$ bunzip2 -k boduo.bz2
```

```shell
$ tar -xjf Japan.tar.bz2
```

### 总结

.gz			gzip	gunzip(gzip -d)

.tar			tar -cf -xf

.tar.gz		tar -zcf -zxf

.zip			zip -r 	unzip

.bz2			bzip2 bunzip2

.tar.bz2	tar -cjf	tar	-xjf	

## 4.7 网络命令

> 网络命令 : `write`

指令名称 : `write`

指令所在路径 : /usr/bin/`write`

执行权限 : 所有用户

语法 : `write` < 用户名 >

功能描述 : 给用户发信息 , 以Ctrl+D保存结束

范例 : 

```shell
# write linzhiling
```

> 网络命令 : wall

指令名称 : `wall`

命令英文原意 : `w`rite `all`

指令所在路径 : usr/bin/`wall`

执行权限 : 所有用户

语法 : `wall` [ message]

功能描述 : 发广播信息

范例 :

```shell
# wall ShenChao is honest man!
```

> 网络命令 : `ping`

命令名称 : `ping`

命令所在路径 : /bin/`ping`

执行权限 : 所有用户

语法 : ` ping` 选项 ip地址 

​								-c   指定发送次数

功能描述 : 测试网络连通性

范例 : 

```shell
# ping 192.168.0.157
```

> 网络命令 : `ifconfig`

命令名称 : `ifconfig`

命令英文原意 : `i`nter`f`ace `config`ure

命令所在路径 : /sbin/`ifconfig

执行权限 : root

语法 : `ifconfig` 网卡名称 IP地址

功能描述 : 查看和设置网卡信息

范例 : 

```shell
# ifconfig eth0 192.168.0.157
```

>网络命令 : `mail`

命令名称 : `mail`

命令所在路径 : /bin/`mail`

执行权限 : 所有用户

语法 : `mail`[ 用户名]

功能描述 : 查看发送电子邮件 

范例 : 

```shell
# mail root
```

>网络命令 :` last`

命令名称 : `last`

命令所在路径 : /usr/bin/`last`

执行权限 : 所有用户

语法 : `last`

功能描述 : 列出目前与过去登入系统的用户信息

范例 : 

```shell
# last
```

> 网络命令 :` lastlog`

命令名称 : `lastlog`

命令所在路径 : /usr/bin/`lastlog`

执行权限 : 所有用户

语法 : `lastlog`

功能描述 : 检查某特定用户上次登录时间

范例 : 

```shell
# lastlog
```

```shell
# last -u 502
```

> 网络命令 : `traceroute`

命令名称 :` traceroute`

命令所在路径 : /bin/`traceroute`

执行权限 : 所有用户

语法 : `traceroute`

功能描述 : 显示数据包到主机间的路径

范例 :

```shell
# traceroute www.lampbrother.net
```

> 网络命令 : `netstat`

命令名称 : `netstat`

命令所在路径 : /bin/`netstat`

执行权限 : 所有用户

语法 : `netstat` [ 选项 ]

功能描述 : 显示网络相关信息

选项 : 

​	-t	 :		TCP协议

​	-u	: 	  UDP协议

​	-l	 :		监听

​	-r	 :		路由

​	-n	:		显示ip地址和端口号

范例 :

```shell
# netstat -tlun			查看本机监听的端口
```

```shell
# netstat -an			查看本机所有的网络连接
```

```shell
# netstat -rn			查看本机路由表
```

> 网络命令 :` setup`

命令名称 : `setup`

命令所在路径 : /usr/bin/`setup`

执行权限 : root

语法 : `setup`

功能描述 : 配置网络 

范例 : 

```shell
# setup
```

> 挂载命令

命令名称 : `mount`

命令位置 : /bin/`mount`

执行权限 : 所有用户

命令语法 : mount [-t 文件系统] 设备文件名 挂载点

范例 :

```shell
# mount -t ios9660 /dev/sr0 /mnt/cdrom
```

## 4.8 关机重启命令

> 1、`shutdown`命令

[ root@localhost~]# shutdown [选项] 时间

​	选项 :

​				-c : 取消前一个关机命令

​				-h : 关机

​				-r : 重启

> 2、 其他关机命令

- [ root@localhost~]# #hlat
- [ root@localhost~]# poweroff
- [ root@localhost~]# init 0

> 3、其他重启命令

- [ root@localhost~]#  reboot
- [ root@localhost~]#  init 6

> 4、系统运行级别 ？

- 0	关机
- 1	单用户
- 2	不完全多用户 , 不含NFS服务
- 3	完全多用户
- 4	未分配
- 5	图形界面
- 6	重启

[ root@localhost~]#   cat /etc/inittab

#修改系统默认运行级别

id:3:initdefault:



[ root@localhost~]#  runlevel

#查询系统运行级别

> 5、退出登录命令

[ root@localhost~]#   logout

## 4.9 各文件的颜色

下面是linux系统约定不同类型文件默认的颜色：

白色：表示普通文件

蓝色：表示目录

绿色：表示可执行文件

红色：表示压缩文件

浅蓝色：链接文件

红色闪烁：表示链接的文件有问题

黄色：表示设备文件

灰色：表示其它文件



# 5. 文本编辑器`Vim`

`Vim`是一个功能强大的全屏幕文本编辑器,是`Linux/UNIX`上最常用的文本编辑器,它的作用是建立、编辑、显示文本文件.

`Vim`没有菜单,只有命令.

www.vim.org

## 5.1 `Vim`常用操作

![image-20200928181709908](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200928181709908.png)

> 插入命令

| 命令 | 作用                 |
| ---- | -------------------- |
| a    | 在光标所在字符插入   |
| A    | 在光标所在的行尾插入 |
| i    | 在光标所在字符前插入 |
| I    | 在光标所在行行首插入 |
| o    | 在光标下插入新行     |
| O    | 在光标上手稿新行     |

> 定位命令

| 命令     | 使用 |
| ---------- | ---- |
| :  set nu  | 设置行号 |
| :s et nonu | 取消行号 |
| gg         | 到第一行 |
| G          | 到最后一行 |
| nG        | 到第n行 |
| : n        | 到第n行 |
| $ | 移至行尾 |
| 0 | 移至行首 |

> 删除命令

| 命令    | 作用                         |
| ------- | ---------------------------- |
| x       | 删除光标所在的处字符         |
| nx      | 删除光标所在处后n个字符      |
| dd      | 删除光标所在行,ndd删除n行    |
| dG      | 删除光标所丰行到文件末尾内容 |
| D       | 删除光标所在处到行尾内容     |
| :n1,n2d | 删除指定范围的行             |

> 复制和剪切命令

| 命令 | 作用                         |
| ---- | ---------------------------- |
| yy   | 复制当前行                   |
| nyy  | 复制当前行以下n行            |
| dd   | 前切当前行                   |
| ndd  | 剪切当前以下n行              |
| p、P | 粘贴在当前光标所在行下或行下 |

> 替换和取消命令

| 命令 | 作用                               |
| ---- | ---------------------------------- |
| r    | 取代光标所在处字符                 |
| R    | 从光标所在处开始替换字符,按Esc结束 |
| u    | 取消上一步操作                     |

> 搜索和搜索替换命令

| 命令              | 作用                                         |
| ----------------- | -------------------------------------------- |
| /string           | 搜索指定字符串 <br />搜索时忽略大小写:set ic |
| n                 | 拂过指定字符串的下一个出现位置               |
| :%s/old/new/g     | 全文替换指定字符串                           |
| :n1,n2s/old/new/g | 在一定范围内替换指定字符串                   |

> 保存和退出命令

| 命令            | 作用                                   |
| --------------- | -------------------------------------- |
| :w              | 保存修改                               |
| :w new_filename | 另存为指定文件                         |
| :wq             | 保存修改并退出                         |
| ZZ              | 快捷键,保存修改并退出                  |
| :q!             | 不保存修改退出                         |
| :wq!            | 保存修改并退出(文件所有者及root可使用) |

## #总结:

vim 命令模式	插入模式		编辑模式

插入命令	aio

定位 	:set nu 		:n

删除	x	nx	dd	ndd

复制和剪切	yy-p	dd-p	

替换和恢复	r/R	u

搜索和替换	/关键词		n			:范围/要替换关键词/替换为关键词/g

保存退出	:wq	ZZ		:q!		




## 5.2 `Vim`使用技巧

导入命令执行结果 : r ！命令

定义快捷键 :map	快捷键 触发命令

范例 : map ^P I#<ESC>

​			: map ^B 0x

连续行注释 : 

​							:n1.n2s/^/#/g

​							:n1,n2s/^#//g

​							:n1,n2s/^/\/\//g

替换 : ab mymial samlee@lampbrother.net

### 总结

vim /root/.vimrc    #配置vim文件



set nu

map ^P I#<ESC>   #插入#号

ab  mymail samlee@lampbrother.net     定义快捷定义

ab shenchao fengjie

# 6. 软件包管理

## 一、软件包简介

### 1、软件包分类

- 源包类
  - 脚本安装包
- 二进制包

### 2、源码包

源码包的优点是:

- 开源,如果有足够的能力,可以修改源代码
- 可以自由选择所需的功能
- 软件是编译安装,所以更加适合自己的系统,更加稳定也效率更高
- 卸载方便

源码包的缺点

- 安装过程步骤多,尤其安装较大的软件集合时(如LAMP环境搭建),容易出现拼写错误
- 编译过程时间较长,安装比二进制安装时间长
- 因为是编译安装,安装过程中一旦报错新手很难解决

### 3、RPM包

二进制包的优点

- 包管理系统简单,只通过几个命令就可以实现包的安装、升级、查询和卸载.
- 安装速度比源码包安装快的多

二进制包缺点:

- 经过编译,不再可以看到源代码
- 功能选择不如源码包灵活
- 依赖性

## 二、RPM包管理-rpm命令管理

###  6.2.1 rpm命令管理-包命名与依赖性#### 1、RPM包命名原则

httpd-2.2.15-15.e16.centos.1.i686.rpm

httpd							软件包名

2.2.15							软件版本

15									软件发布的次数

e16.centos					适合的Linux平台

i686 								适合的硬件平台

rpm								rpm包扩展名

#### 2、RPM包依赖性

- 树形依赖: a-> b -> c
- 环形依赖 : a -> b -> c -> a
- 模块依赖 : 模块依赖查询网站 : www.rpmfind.net



### 6.2.2 rpm命令管理-安装升级与卸载

####  1、包全包与包名

- 包全名 : 操作的包是没有安装的软件包时,使用包全名 . 而且要注意路径
- 包名 : 操作已经安装的软件包时 , 使用包名 . 是搜索/var/lib/rpm/中的数据库

#### 2、`RPM`安装

`rpm`-ivh 包全名

选项:

​			-i	( intsall )				安装

​			-v	( verbose )			显示详细信息

​			-h	( bash )				 显示进度

​			--nodeps						不检查依赖性

#### 3、 ` RPM`包升级

`rpm` -Uvh 包全名

​			-U	( upgrade )					升级

​			-v	( verbose )					显示详细信息

​			-h	( bash )						 显示进度

#### 4、 卸载

`rpm` -e 包名

选项 :

​			-e ( erase)						卸载

​			--nodeps							不检查依赖性



### 6.2.3 rpm命令管理-查询

#### 1、 查询是否安装

[root@localhost~]# rpm -q 包名

#查询包是否安装

选项 : 

​			-q				查询	( query )

[root@localhost~]#rpm -qa

#查询所有已经安装的RPM包

选项 : 

​			-a 				所有( all )

#### 2、查询软件包详细信息

[root@localhost~]# rpm -qi 包名

选项 : 

​			-i			查询软件信息 ( information)

​			-p			查询未安装包的信息 ( package)

#### 3、查询包中文件安装位置

[root@localhost~]# rpm -ql 包名

选项 : 	

​			-l				列表( list)

​			-p				查询未安装包信息( package)

#### 4、查询系统文件属于哪个RPM包

[root@localhost~]# rpm -qf	系统文件名

选项 :	

​			-f 			查询系统文件属于哪个软件包( file)

#### 5、 查询软件包的依赖性

[root@localhost~] # rpm -qR 包名

选项 :

​		-R 查询软件包的依赖性 ( requires )

​		-p 查询未安装包信息	( package)

### 6.2.4 rpm命令管理-校验和文件提取

#### 1、RPM包校验

[root@localhost~]# rpm -V 已安装的包名

选项:

​			-V		校验指定RPM包中的文件	( verify)

> 验证内容中的8个信息的具体内容如下 :

- S			文件大小是否改变
- M			文件的类型或文件权限 ( rwx )是否被改变
- S			文件MD5校验和是否改变	(可以看成文件内容是否改变)
- D			设备的中,从代码是否改变
- L			文件路径是否改变
- U			文件的属主(所有者)是否改变
- G			文件的属组是否改变
- T			文件的修改时间是否改变

> 文件类型

- c					配置文件 ( config file)
- d					普通文档( documentation )
- g					“鬼” 文件 (ghost file) ,很少见 ,就是该文件不应该被这个RPM包包含
- l					授权文件( license file)
- r					描述文件 (read me)

#### 2、RPM包中文件提取

[root@localhost~]# rpm2cpio 包全名 | \

cpio -idv .文件绝对路径



rpm2cpio

#将rpm包转换为cpio格式的命令

cpio

#是一个标准工具,它用于创建软件档案文件和从档案文件中提取文件

[root@localhost~]# cpio 选项 <[ 文件设备 ]

选项 : 

​			-i:		copy-in模式,还原

​			-d:		还原时自动新建目录

​			-v:		显示还原过程

```shell
[root@localhost~]# rpm -qf /bin/ls
```

#查询ls命令属于哪个软件包

```shell
[root@localhost~]# mv /bin/ls /tmp/
```

#造成ls命令误删除假象

```shell
[root@localhost~]# rpm2cpio /mnt/cdrom/Packages/coreutlis-8.4-19.e16.i686.rpm | cpio -idv ./bin/ls
```

#提取RPM包中ls命令到当前目录的/bin/ls下

```shell
[root@localhost~]# cp /root/bin/ls /bin/
```

#把ls命令复制到/bin/目录 ,修复文件丢失

## 三、PRM包管理-yum在线管理

### 6.3.1 yum在线管理-IP地址配置和网络yum源

#### 1、IP地址配置

```shell 
[root@localhost~]# setup
```

#使用setup工具

```shell
[root@localhost~]# vim /etc/sysconfig/network-scripts/ifcfg-eth0
```

把ONBOOT=“no”改为

ONBOOT=“yes”

#启动网卡



```shell
[root@localhost~]# service network restart
```

#重启网络服务

#### 2、网络yum源

```shell
[root@localhost~]# vim /etc/yum.repos.d/CentOS-Base.repo
```

- [base]			容器名称,一定要放在[]中

- name           容器说明,可以自己随便写

- mirrorlist     镜像站点,这个可以注释掉

- baseurl        我们的yum源服务器地址.默认是CentOS官方的yum源服务器,是可以使用的,如果你觉得慢可以改你            

  ​                     喜欢的yum源地址

- enabled       此容器是否生效,如果不写或写成enable=1都是生效,写成enable=0 就是不生效

- gpgcheck     如果是1是指RPM的数字证书生效,如果是0则不生效

- gpgkey         数字证书的公钥文件保存位置 . 不用修改

![image-20200929064755006](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929064755006.png)

> 改阿里去源地址

https://developer.aliyun.com/mirror/centos?spm=a2c6h.13651102.0.0.3e221b11fFuhKH

>  CentOS 镜像

>  简介

CentOS，是基于 Red Hat Linux 提供的可自由使用源代码的企业级 Linux 发行版本；是一个稳定，可预测，可管理和可复制的免费企业级计算平台。

>  配置方法

> 1. 备份

```shell
mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup
```

>  2. 下载新的 CentOS-Base.repo 到 /etc/yum.repos.d/

**CentOS 6**

```shell
wget -O /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-6.repo
```

或者

```shell
curl -o /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-6.repo
```

**CentOS 7**

```shell
wget -O /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-7.repo
```

或者

```shell
curl -o /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-7.repo
```

**CentOS 8**

```shell
wget -O /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-8.repo
```

或者

```shell
curl -o /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-8.repo
```

>  3. 运行 yum makecache 生成缓存

>  4. 其他

非阿里云ECS用户会出现 Couldn't resolve host 'mirrors.cloud.aliyuncs.com' 信息，不影响使用。用户也可自行修改相关配置: eg:

```shell
sed -i -e '/mirrors.cloud.aliyuncs.com/d' -e '/mirrors.aliyuncs.com/d' /etc/yum.repos.d/CentO
```

![image-20200929065748173](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929065748173.png)

### 6.3.2 yum命令

#### 1、常用yum命令

>  1)	查询

```shell
[root@localhost yum.repos.d]# yum list
```

#查询所有可用软件包列表

```shell
[root@localhost yum.repos.d]# yum search 关键字
```

#搜索服务器上所有和关键字相关的包

>  2)	安装

```shell
[root@localhost yum.repos.d]# yum -y install 包名
```

install 			安装

-y 					自动回答yes

```shell
[root@localhost ~]# rpm -q gcc
```

​	如果没安装则安装gcc

```shell
[root@localhost ~]# yum -y install gcc
```

>  3)	升级

```shell
[root@localhost ~]# yum -y update	包名
```

选项:

​			update		升级

​			-y					自动回答yes

> 4)	卸载

[root@localhost ~]# yum -y remove	包名

选项:

​			remove		卸载

​			-y					自动回答yes

#### 2、YUM软件组管理命令

```shell
[root@localhost ~]# yum grouplist
```

#列出所有可用的软件组列表

```shell
[root@localhost ~]# yum groupinstall 软件组名
```

#安装指定软件组,组名可以由grouplist查询出来

```shell
[root@localhost ~]# yum groupremove 软件组名
```

#卸载指定软件组

### 6.3.3 光盘yum源搭建

> 光盘yum源搭建步骤

1) 挂载光盘

```shell
[root@localhost ~]# mount /dev/sr0	/mnt/cdrom/
```

2)让网络yum原文件失效

```shell
[root@localhost ~]#cd /etc/yum.repos.d/
[root@localhost yum.repos.d]#mv CentOS-Base.repo CentOS-Base.repo.bak
[root@localhost yum.repos.d]#mv CentOS-Debuginfo.repo CentOS-Debuginfo.repo.bak
[root@localhost yum.repos.d]#mv CentOS-Vault.repo CentOS-Vault.repo.bak
```

3) 修改光盘yum源文件

```shell
[root@localhost yum.repos.d]# vim CentOS-Media.repo
[c6-media]
name=CentOS-$releasever-Media
baseurl=file:///mnt/cdrom
#地址为你自己的光盘挂载地址

#	file:///media/cdrom/

#	file:///media/cdrecorder/

#注释这两个不存在的地址

gpgcheck=1

enabled=1

#把enabled=0 改为enabled=1 , 让这个yum源配置文件生效

gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6


```

## 四、 源码包管理

### 6.4.1 源码包和RPM包的区别

#### 1、区别

- 安装之前的区别 : 概念上的区别
- 安装之后的区别 : 安装位置不同

#### 2、RPM包安装位置

- PRM包默认安装路径

| /etc/           | 配置文件安装目录           |
| --------------- | -------------------------- |
| /usr/bin/       | 可执行的命令安装目录       |
| /usr/lib/       | 程序所使用的函数库保存位置 |
| /usr/share/doc/ | 基本的软件使用手册保存位置 |
| /usr/share/man/ | 帮助文件保存位置           |

#### 3、源码包安装位置

- 安装在指定位置当中,一般是/usr/local/软件名/

#### 4、安装位置不同带来的影响

- PRM包安装的服务可以使用系统服务管理命令( service)来管理,例如RPM包安装的apache的启动方法 是:

  - /etc/rc.d/init.d/httpd start

  - service httpd start

- 而源码包安装的服务则不能被服务管理命令管理,因为没有安装到默认路径中.所以只能用绝对路径进行服务的管理,如:

  - ```shell
    /usr/local/apache2/bin/apachectl start
    ```

### 6.4.2 源码包安装过程

#### 1、安装准备

- 安装C语言编译器
- 下载源码包

http://mirror.bit.edu.cn/apache/httpd/

#### 2、安装注意事项

- 源代码保存位置 : /usr/local/src/
- 软件安装位置 : /usr/local/
- 如何确定安装过程报错 :
  - 安装过程停止
  - 并出现eroor、warning或no的提示

####  3、源码包安装过程

- 下载源码包
- 解压缩下载的源码包
- 进入解压缩目录

- ./configure 软件配置与检查
  - 定义需要的功能选项 .
  - 检测系统环境是否符合安装要求 .
  - 把定义好的功能选项和检测系统环境的信息都写入Makefile文件,用于后续的编辑.
- make      编译
  - make clean
- make install     编译安装

**测试运行**

```shell
[root@localhost httpd-2.2.9]# /usr/local/apache2/bin/apachectl start

解决apache启动错误"httpd:Could not reliably determine..."
[root@localhost httpd-2.2.9]# vim /usr/local/apache2/conf/httpd.conf 
编辑httpd.conf文件，搜索"#ServerName"，添加ServerName localhost:80

还是访问不了网页的话,那关闭防火墙
[root@localhost httpd-2.2.9]# service iptables stop

最后打开网站 192.168.0.188 
```

![image-20200929232456913](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929232456913.png)

#### 4、源码包的卸载

- 不需要卸载命令 , 直接删除安装目录即可 .

不会遗留任何垃圾文件.

```shell
[root@localhost httpd-2.2.9]# rm -rf /usr/local/apache2/
```

![image-20200929232836486](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929232836486.png)

## 五、脚本安装包与软件包选择

### 1、脚本安装包

- 脚本安装包并不是独立的软件包类型 , 常见安装的是源码包 .
- 是人为把安装过程写成了自动安装的脚本 , 只要执行脚本 , 定义简单的参数 , 就可以完成安装 .
- 非常类似于 Windows下软件的安装方式 .

### 2、Webmin的作用

Webmin 是一个基于 Web 的Linux 系统管理界面 . 您就可以通过图形化的方式设置用户帐号、Apache、DNS、文件共享等服务 .

### 3、Webmin安装过程

- 下载软件
  - http://sourceforge.net/projects/webadmin/files/webmin/

- 解压缩,并进入加压缩目录
- 执行安装脚本

# 7. 用户和用户组管理

## 7.1 用户配置文件

### 7.1.1 用户信息文件 /etc/passwd

#### 7.1.1.1 用户管理简介

- 所以越是对服务器安全性要求高的服务器,越需要建立合理的用户权限等级制度和服务器操作规范 .
- 在 Linux 中主要是通过用户配置文件来查看和修改用户信息

#### 7.1.1.2 /etc/passwd

- 第1字段 : 用户名称
- 第2字段 : 密码标志
- 第3字段 : UID (用户ID)
  - 0:				      超级用户
  - 1-499:		     系统用户(伪用户)
  - 500-65535:    普遍用户
- 第4字段 : GID (用户初始组ID)
- 第5字段 : 用户说明
- 第6字段 : 家目录
  - 普遍用户: /home/用户名/
  - 超级用户: /root/
- 第7字段 : 登录之后的Shell

#### 7.1.1.3 初始组和附加组

- 初始组 : 就是指用户一登录就立刻拥有这个用户组的相关权限 , 每个用户的初始组只能有一个,一般就是和这个用户的用户名相同的组名作为这个用户的初始组 .
- 附加组 : 指用户可以加入多个其他的用户组 , 并拥有这些组的权限 , 附加组可以有多个 .

#### 7.1.14 `Shell`是什么

- `Shell`就是Linux的命令解释器 .
- 在/etc/passwd当中 , 除了标准Shell是/bin/bash之外,还可以写如 /sbin/nologin .

### 7.1.2 影子文件 /etc/shadow

#### 7.1.2.1 影子文件 /etc/shadow

- 第1字段 : 用户名

- 第2字段 : 加密密码

  - ​	 加密算法升级为SHA512散列加密算法

  - ​	 如果密码位是“!!”或“*”代表没有密码,不能登录

- 第3字段 : 密码最后一次修改日期
  - ​	使用1970年1月1日作为标准时间 , 每过一天时间戳加1
- 第4字段 : 两次密码的修改间隔时间 和(第3字段相比)
- 第5字段 : 密码有效期 (和第3字段相比)
- 第6字段 : 密码修改到期前的警告天数(第5字段相比)
- 第7字段 : 密码过期后的宽限天数(和第5字段相比)
  - 0: 代表密码过期后立即失效
  - -1: 则代表密码永远不会失效 .
- 第8字段 : 帐号失效时间
  - 要用时间戳表示
- 第9字段 : 保留

#### 7.1.2.2 时间戳换算

- 把时间戳换算为日期

  - data -d “1970-01-01 160066 days”

- 把日期换算为时间戳

  - ```shell
    echo $ (($(date --date="2014/01/06"+%s)/86400+1))
    ```



### 7.1.3 组信息文件 /etc/gruop 和组密码文件 /etc/gshadow

#### 7.1.3.1 组信息文件 /etc/group

- 第一字段 : 组名
- 第二字段 : 组密码标志
- 第三字段 : GID
- 第四字段 : 组中附加用户 

#### 7.1.3.2 组密码文件/etc/gshadow

第一字段 : 组名

第二字段 : 组密码

第三字段 : 组管理员用户名

第四字段 : 组中附加用户

## 7.2 用户管理相关文件

#### 7.2.1.1 用户的家目录

普通用户 : /home/用户名/,所有者和所属组都是此用户 ,权限是700

超级用户 : /root/ ,所有者和所属组都是root,权限是550

#### 7.2.1.2 用户的邮箱

- /var/spool/mail/用户名/

#### 7.2.1.3 用户模板目录

- /etc/skel

## 7.3 用户管理命令

### 7.3.1 用户添加命令 useradd

#### 7.3.1.1 useradd命令格式

```shell
[root@localhost ~]# useradd [选项]用户名
```

选项:

​			-u	UID:				手工指定用户的UID号

​			-d	家目录:		手工指定用户的家目录

​			-c	用户说明:	手工指定用户的说明

​			-g 	组名:			手工指定用户的初始组

​			-G 	组名:			指定用户的附加组

​			-s 	shell:			手工指定用户的登录shell . 默认是/bin/bash

#### 7.3.1.2 添加默认用户

- ```shell
  [root@localhost ~]# useradd sc
  ```

  - ```shell
    [root@localhost ~]# grep sc /etc/passwd
    ```

  - ```shell
    [root@localhost ~]# grep sc /etc/shadow
    ```

  - ```shell
    [root@localhost ~]# grep sc /etc/group
    ```

  - ```shell
    [root@localhost ~]# grep sc /etc/gshadow
    ```

  - ```shell
    [root@localhost ~]# ll -d /home/lamp/
    ```

  - ```shell
    [root@localhost ~]# ll /var/spool/mail/lamp
    ```

#### 7.3.1.3 指定选项添加用户

- ```shell
  useradd -u 550 -G root,bin -d /home/lamp1 -c "test user" -s /bin/bash sc
  ```

#### 7.3.1.4 用户默认值文件

- /etc/default/useradd
  - GROUP=100			#用户默认组
  - HOME=/home       #用户家目录
  - INACTIVE=-1          #密码过期宽限天数(shadow文件7字段)
  - EXPIRE=                 #密码失效时间( 8 )
  - SHELL=/bin/bash  #默认shell
  - SKEL=/etc/skel      #模板目录
  - CREATE_MAIL_SPOOL=yes       #是否建立邮箱
- /etc/login.defs
  - PASS_MAX_DAYS 99999	#密码有效期( 5 )
  - PASS_MIN_DAYS 0            #密码修改间隔( 4 )
  - PASS_MIN_LEN 5              #密码最小5位( PAM )
  - PASS_WARN_AGE 7           #密码到期警告 ( 6 )
  - UID_MIN 500                      # 最小和最大UID范围
  - GID_MAX 60000                  
  - ENCRYPT_METHOD   SHA512   #加密模式



### 7.3.2 修改用户密码 passwd

#### 7.3.2.1 passwd命令格式

[root@localhost ~]# passwd [选项]用户名

选项:

​			-S			查询用户密码的密码状态 . 仅root用户可用.

​			-l			暂时锁定用户.仅root用户可用.

​			-u  		解锁用户 . 仅root用户可用 .

​			--stdin 可以通过管道符输出的数据作为用户的密码.

#### 7.3.2.2 查看密码状态

[root@localhost ~]# passwd -S lamp

lamp PS 2013-03-06 0 99999 7 -1

2013-03-06	#用户名密码设定时间 

0 	#密码修改间隔时间

99999 		#密码有效期

7				#警告时间

-1			  #密码不失效

#### 7.3.2.3 锁定用户和解锁用户

[root@localhost ~]# passwd -l lamp

[root@localhost ~]# passwd -u lamp

#### 7.3.2.4 使用字符串作为用户的密码

[root@localhost ~]# echo “123” | passwd  --stdin lamp



### 7.3.3 修改用户信息usermod

				### 			修改用户密码状态change

#### 7.3.3.1 修改用户信息usermod

[root@localhost ~]# usermod [选项] 用户名

选项:

​			-u UID:					修改用户的UID号

​			-c 用户说明:		修改用户的说明信息

​			-G 组名:				修改用户的附加组

​			-L:							临时锁定用户( Lock )

​			-U:							解锁用户锁定( Unlock )

[root@localhost ~]# usermod -c “test uesr” lamp

#修改用户的说明

[root@localhost ~]# usermod -G root lamp

#把lamp用户加入root组

[root@localhost ~]#  usermod -L lamp

#锁定用户

[root@localhost ~]#  usermod -U lamp

#解锁用户

#### 7.3.3.2 修改用户密码状态 chage

[root@localhost ~]# chane [选项] 用户名

选项:

​			-l:						列出用户的详细密码状态

​			-d 日期:			修改密码最后一次更新日期(shadow 3字段)

​			-m 天数:			两次密码修改间隔 ( 4 字段)

​			-M 天数:			 密码有效期(5字段)

​			-W 天数:			密码过后宽限天数 ( 7字段 )

​			-E 日期:			帐号失效时间 (8字段)

[root@localhost ~]# chage -d 0 lamp

#这个命令其实是把密码修改日期归0了 (shadow 第3字段)

#这样用户一登录就要修改密码





### 7.3.4 删除用户 userdel

### 			用户切换命令

#### 7.3.4.1 删除用户 userdel

[root@localhost ~]# userdel [-r] 用户名

选项:

​			-r				删除用户的同时删除用户家目录

>  手工删除用户

[root@localhost ~]#  vim /etc/passwd

[root@localhost ~]#  vim /etc/shadow

[root@localhost ~]#  vim /etc/group

[root@localhost ~]#  vim /etc/gshadow

[root@localhost ~]#  rm -rf /var/spool/mail/lamp

[root@localhost ~]#  rm -rf /home/lamp

#### 7.3.4.2 查看用户ID

[root@localhost ~]# id 用户名

#### 7.3.4.3 切换用户身份 su

[root@localhost ~]#  su [选项] 用户名

选项:

​			-: 					选项只使用“-” 代表连带用户的环境变量一起切换

​			-c 命令: 		仅执行一次命令,而不切换用户身份

> [root@localhost ~]#  su -root

#切换成root

>[root@localhost ~]# su -root -c “useradd user3” 

#不切换成root , 但是执行useradd命令添加user1用户



## 7.4 用户组管理命令

### 7.4.1 添加用户组

[root@localhost ~]# groupadd [选项] 组名

选项:

​			-g  GID:					指定组ID

### 7.4.2 修改用户组

[root@localhost ~]#  groupmod [选项] 组名

选项:

​			-g GID:				修改组ID

​			-n 新组名:		修改组名

[root@localhost ~]#  groupmod -n testgrp group1

#把组名group1 修改为testgrp

### 7.4.3 删除用户组

[root@localhost ~]#  groupdel 组名

### 7.4.4 把用户添加入组或从组中删除

[root@localhost ~]# gpasswd 选项 组名

选项:

​			-a 用户名:					把用户加入组

​			-d 用户名:					把用户从组中删除

# 8. 权限管理

## 8.1 ACL权限

### 8.1.1 ACL权限简介与开启

#### 8.1.1.1 ACL权限简介

ACL 是Access Contol list的英文缩写 ,中文译为访问控制列表 , 主要目的是提供传统的属主、所属群组、其他人的读、写、执行权限之外的详细权限设置.

![image-20200930050144436](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930050144436.png)

#### 8.1.1.2 查看分区ACL权限是否开启

[root@localhost ~]# dumpe2fs -h /dev/sda3

#dumpe2fs命令是查询指定分区详细文件系统信息的命令

选项:

​			-h 		仅显示超级块中信息,而不显示磁盘块组的详细信息

#### 8.1.1.3 临时开启分区ACL权限

[root@localhost ~]# mount -o remount,acl /

#重新挂载根分区 ,并挂载加入acl权限

#### 8.1.1.4 永久开启分区ACL权限

[root@localhost ~]# vim /etc/fstab

UUID=0c28f491-5fa6-4911-9e93-8bc07f17600e /                       ext4    defaults ,acl       1 1

#加入acl

[root@localhost ~]# mount -o remount /

#重新挂载文件系统或重启动系统,使修改生效



> 

### 8.1.2 查看与设定ACL权限

#### 8.1.2.1 查看ACL命令

[root@localhost ~]# getfacl 文件名

#查看acl权限

#### 8.1.2.2 设定ACL权限的命令

[root@localhost ~]# setfacl 选项 文件名

选项:

​			-m			设定ACL权限

​			-x 			 删除指定的ACL权限

​			-b			  删除所有的ACL权限

​			-d			  设定默认ACL权限

​			-k     	    删除默认ACL权限

​			-R			   递归设定ACL权限

#### 8.1.2.3 给用户设定ACL权限

![image-20200930054335341](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930054335341.png)

```shell
[root@localhost weqq01]# gpasswd -a weqq01 tgroop
[root@localhost weqq01]# gpasswd -a weqq02 tgroop
[root@localhost weqq01]# gpasswd -a weqq03 tgroop
[root@localhost weqq01]# groupadd  tgroop
[root@localhost weqq01]# mkdir project
[root@localhost weqq01]# chown root:tgroup /project/
[root@localhost weqq01]# chmod 770 /project/
[root@localhost weqq01]# setfacl -m u:st:rx /project/
```

#给用户st赋予r-x权限,使用“u:用户名:权限”格式

#### 8.1.2.4 给用户组设定ACL权限

[root@localhost /]# groupadd tgroup2

[root@localhost /]# setfacl -m g:tgroup2:rwx project/



>

### 8.1.3 最大有效权限与删除ACL权限

#### 8.1.3.1 最大有效权限mask

mask是用来指定最大有效权限的 . 如果我给用户赋予了ACL权限,是需要和mask权限“相与”才能得到用户的真正权限.

![image-20200930061109612](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930061109612.png)

修改最大有效权限

[root@localhost ~]# setfacl -m m:rx 文件名

#设定mask权限为r-x . 使用“m:权限”格式

#### 8.1.3.2 删除ACL权限

[root@localhost ~]# setfacl -x u:用户名 文件名

#删除指定用户的ACL权限

[root@localhost ~]# setfacl -x g:组名文件名

#删除指定的用户组的ACL权限

[root@localhost ~]# setfacl -b 文件名

#会删除文件的所有的ACL权限

> 

### 8.1.4 默认ACL权限和递归ACL权限

#### 8.1.4.1 递归ACL权限

- 递归是父目录在设定ACL权限时,所有的子文件和子目录也会拥有相同的ACL权限 .
- setfacl -m u: 用户名 : 权限 -R 文件名

![image-20200930062406720](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930062406720.png)

#### 8.1.4.2 默认ACL权限

- 默认ACL权限的作用是如果给父目录设定了默认ACL权限,那么父目录中所有新建的子文件都会继承父目录的ACL权限.
- setfacl -m d:u:用户名:权限 文件名

> 

## 8.2 文件特殊权限

### 8.2.1 SetUID

> 

#### 8.2.1.1 SetUID的功能

- 只有可以执行的二进制程序才能设定SUID权限

- 命令执行者要对该程序拥有x(执行)权限

- 命令执行者在执行该程序时获得该程序文件属主的身份( 在执行程序的过程中灵魂联附体为文件的属主)

- SetUID权限只在该程序执行过程中有效,也就是身份改变只在程序执行过程中有效

- passwd命令拥有SetUID权限,所以普通可以修改自己的密码

  - [root@localhost ~]# ll /usr/bin/passwd

    -rw`s`r-xr-x. 1 root root 25980 2月 22 2012 /usr/bin/passwd

- cat命令没有SetUID权限,所以普通用户不能查看/etc/shadow文件内容

  - [root@localhost ~]# ll /bin/cat

    -rwxr-xr-x root root 47976 6月 22 2012 /bin/cat

![image-20200930073721603](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930073721603.png)

> 

#### 8.2.1.2 设定SetUID的方法

- 4 代表SUID
  - chmod 4775 文件名
  - chmod u+s 文件名

> 

#### 8.2.1.3 取消SetUID的方法

- chmod 755 文件名
- chmod u-s 文件名

> 

#### 8.2.1.4 危险的SetUID

- 关键目录应严格控制写权限 . 比如 “/”、“/usr”等
- 用户的密码设置要严格遵守密码三原则
- 对系统中默认应该具有SetUID权限的文件作一列表,定时检查有没有这之外的文件被设置了SetUID权限

> 

### 8.2.2 SetGID

> 

#### 8.2.2.1 SetGID针对文件的作用

- 只有可执行的二进制程序才能设置SGID权限
- 命令执行者要对该程序拥有x(执行)权限
- 命令执行在执行程序的时候,组身份升级为该程序文件的属组
- SetGID权限同样只在该程序执行过程有效,也就是说组身份改变只在程序执行过程中有效

#### 8.2.2.2 SetGID针对目录的作用

- 普通用户必须对此目录拥有r和x权限,才能进入此目录
- 普通用户在此目录中的有效组会变成此目录的属组
- 若普通用户对此目录拥有w权限时,新建的文件的默认属组是这个目录的属组

[root@localhost ~]#  ll /usr/bin/locate

-rwx--s--x. 1 root slocate 42032 8月  24 2010 /usr/bin/locate

[root@localhost ~]# ll /var/lib/mlocate/mlocate.db

-rw-r-----. 1 root slocate 2921966 9月  30 03:38 /var/lib/mlocate/mlocate.db

- /usr/bin/locate是可执行二进制程序,可以赋予SGID
- 执行用户lamp对/usr/bin/locate命令拥有执行权限
- 执行/usr/bin/locate命令时,组身份会升级为slocate组,而slocate组对/var/lib/mlocate/mlocate.db数据库拥有r权限,拟普通用户可以使用locate命令查询mlocate.db数据库
- 命令结束,lamp用户的组身份返回到lamp组

#### 8.2.2.3设定SetGID

- 2代表SGID
  - chmod 2755 文件名
  - chmod g+s 文件名

```shell
[root@localhost ~]# cd /tmp/
[root@localhost tmp]# mkdir dtest
[root@localhost tmp]# ll -d dtest
drwxr-xr-x. 2 root root 4096 9月  30 04:41 dtest
[root@localhost tmp]# chmod g+s dtest
[root@localhost tmp]# ll -d dtest
drwxr-sr-x. 2 root root 4096 9月  30 04:41 dtest
[root@localhost tmp]# chmod 777 dtest/
[root@localhost tmp]# ll -d dtest
drwxrwsrwx. 2 root root 4096 9月  30 04:41 dtest
[root@localhost tmp]# su - weqq01
[weqq01@localhost ~]$ cd /tmp/dtest/
[weqq01@localhost dtest]$ touch abc
[weqq01@localhost dtest]$ ll
总用量 0
-rw-rw-r--. 1 weqq01 root 0 9月  30 04:42 abc
[weqq01@localhost dtest]$ 

```

#### 8.2.2.4取消SetGID

- chmod 755 文件名
- chmod g-s 文件名

> 

### 8.2.3 Sticky BIT

#### 8.2.3.1 SBIT粘着位作用

- 粘着位目前只对目录有效
- 普通用户对该目录拥有w和x权限,即普通用户可以在此目录拥有写入权限
- 如果没有粘着位,因为普通用户拥有w权限,所以可以删除此目录下所有文件,包括其他用户建立的文件 . 一但赋予了粘着位,除了root可以删除所有文件,普通用户就算拥有w权限,也只能删除自己的建立文件,但是不能删除其他用户建立的文件 .

```shell
[root@localhost ~]# ll -d /tmp/
drwxrwxrwt. 5 root root 4096 9月  30 04:41 /tmp/
```

#### 8.2.3.2 设置与取消粘着位

- 设置粘着位
  - chmod 1755 目录名
  - chmod o+t 目录名
- 取消粘着位
  - chmod 755 目录名
  - chmod o-t 目录名

> 

## 8.3 文件系统属性chattr权限

### 8.3.1 charrt命令格式

```shell
[root@localhost ~]# chattr [+-=][选项]文件或目录名
```

​	+:	增加权限

​	-:	删除权限

​	=:	等于某权限

选项

​		i:	如果对文件设置i属性,那么不允许对文件进行删除、改名,也不能添加和修改数据；如果对目录设置i属性,那么只能修改目录下文件的数据,但不允许建立和删除文件 .

​		a:	如果对文件设置a属性,那么只能在文件中增加数据,但是不能删除也不能修改数据；如果对目录设置a属性,那么只允许在目录中建立和修改文件,但是不允许删除.

### 8.3.2 查看文件系统属性

[root@localhost ~]# lsattr 选项 文件名

选项 : 

​			-a	显示所有文件和目录

​			-d	若目标是目录,仅列出目录本身的属性,而不是子文件的 

> 

## 8.4 系统命令sudo权限

### 8.4.1 sudo权限

- root把本来只能超级用户执行的命令赋予普通用户执行 .
- sudo的操作对象是系统命令

### 8.4.2 sudo使用

[root@localhost ~]# visudo

#实际修改的是/etc/sudoers文件



root				ALL=(ALL)																ALL

#用户名		被管理主机的地址=(可使用身份)			  授权命令(绝对路径)

#%wheel			ALL=(ALL)															ALL

#%组名			被管理主机的地址=( 可使用的身份)		授权命令 ( 绝对路径 )

### 8.4.3 授权sc用户可以重启服务器

[root@localhost ~]#visudo

sc			ALL=/sbin/shutdown -r now

### 8.4.4 普通用户执行sudo赋予的命令

[root@localhost ~]# su - sc

[sc@localhost ~]$ sudo -l

#查看可用的sudo命令

[lamp@localhost ~]$ sudo / sbin/shutdown -r now

#普遍用户执行sudo赋予的命令 

![image-20200930214412210](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930214412210.png)

> 

# 9.  文件系统管理

## 9.1 回顾分区和文件系统

### 9.1.1 分区类型

- 主分区 : 总共最多只能分四个
- 扩展分区 : 只能有一个 , 也算作主分区的一种 , 也就是说主分区加扩展分区最多有四个 . 但是扩展分区不能存储数据和格式化 , 必须再划分逻辑分区才能使用 .
- 逻辑分区 : 逻辑分区是在扩展分区中划分的,如果是IDE硬盘 , Linux 最多支持 59 个逻辑分区 , 如果是SCSI 硬盘Linux最多支持11个逻辑分区

>  分区表示方法 



![image-20200930220029248](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930220029248.png)



![image-20200930220123773](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930220123773.png)

![image-20200930220251584](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930220251584.png)



![image-20200930220300908](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200930220300908.png)

### 9.1.2文件系统

- ext2 : 是ext文件系统的升级版本,Red Hat Linux 7.2 版本以前的系统默认都是ext2 文件系统 . 1993年发布 , 最大支持16TB的分区和最大2TB的文件( 1TB = 1024 GB= 1024*1024KB)

- ext3 : ext3文件系统是etx2文件系统的升级版本,最大的区别就是带日志功能,以在系统突然停止时提高文件系统的可靠性 . 支持最大16GB的分区和最大2TB的文件 .

- ext4 : 它是ext3文件系统的升级版 . ext4 在性能、伸缩性和可靠性方面进行了大量改进 . EXT4 的变化可以说是翻天覆地的 ,比如向下兼容 EXT3 、最大1EB文件系统和16TB文件、无限数量子目录、Extents连续数据块概念、多块分配、延迟分配、持久预分配、快速FSCK、日志校验、无日志模式、在线碎片整理、inode增强、默认启用barrier等 . 是CentOS 6.3的默认文件系统

  (1EB=1024PB=1024*1024TB)

## 9.2 文件系统常用命令

### 9.2.1 df命令、du命令、fsck命令和dump2fs命令

#### 9.2.1.1 文件系统查看命令df

[root@localhsot~]# df [选项] [挂载点]

选项: 

​		-a	显示所有的文件系统信息 , 包括特殊文件系统 , 如 /proc、/sysfs

​		-h	使用习惯单位显示容量,如KB,MB或GB等

​		-T	显示文件系统类型

​		-m	以MB为单位显示容量

​		-k	以KB为单位显示容量 . 默认就是以KB为单位

#### 9.2.1.2 统计目录或文件大小

[root@localhsot~]# du [选项] [目录或文件名]

选项:

​		-a	显示每个子文件的磁盘占用量 . 默认只统计子目录的磁盘占用量

​		-h	使用习惯单位显示磁盘占用量,如KB,MB或GB等

​		-s	统计总占用量,而不列出子目录和子文件的占用量 

> du命令和df命令的区别

- df命令是从文件系统考虑的,不光要考虑文件占用的空间,还要统计被命令和程序占用空间(最常见的就是文件已经删除,但是程序并没有释放空间)
- du命令是面向文件的,只会计算文件或目录占用的空间

#### 9.2.1.3 文件系统修复命令fsck

[root@localhsot~]#  fsck [选项] 分区设备文件名

选项:

​			-a		不用显示用户提示,自动修复文件系统

​			-y		自动修复.和-a作用一致,不过有些文件系统只支持-y

#### 9.2.1.4 显示磁盘状态命令dumpe2fs

[root@localhsot~]# dumpe2fs 分区设备文件名

### 9.2.2 挂载命令

#### 9.2.2.1 查询与自动挂载

[root@localhsot~]#  mount [-l]

#查询系统中已经挂载的设备,-l 会显示卷标名称



[root@localhsot~]#  mount -a

#依据配置文件/etc/fstab的内容,自动挂载

#### 9.2.2.2 挂载命令格式

[root@localhsot~]# mount [-t 文件系统] [-L 卷标名] [-o 特殊选项] 设备文件名 挂载点

选项:

​			-t 文件系统 :	加入文件系统类型来指定挂载的类型,可以ext3、ext4	、ios9660等文件系统

​			-L 卷标名:		 挂载指卷标的分区,而不是安装设备文件名挂载

​			-o 特殊选项:    可以指定挂载的额外选项

| 参数          | 说明                                                         |
| ------------- | ------------------------------------------------------------ |
| atime/noatime | 更新访问时间/不更新访问时间 . 访问分区文件时 ,是否更新文件的访问时间,默认为更新 |
| async/sync    | 异步/同步,默认为异步                                         |
| auto/noauto   | 自动/手动,mount -a命令执行时 , 是否会自动安装/etc/fstab文件内容挂载,默认为自动 |
| defaults      | 定义默认值,相当于rw,suid,dev,exec,auto,nouser,async这个选项  |
| exec/noexec   | 执行/不执行,设定是否允许在文件系统中执行可执行文件,默认是exec允许 |
| remount       | 重新挂载已经挂载的文件系统,是否具有读写权限,默认是rw         |
| rw/ro         | 读写/只读,文件系统挂载时,是否具有读写权限,默认是rw           |
| suid/nosuid   | 具有/不具有SUID权限,设定文件系统是否具有SUID和SGID的权限,默认是具有 |
| user/nouser   | 允许/不允许普通用户挂载,设定文件系统是否允许普通用户挂载,默认是不允许,只有root可以挂载分开 |
| usrquota      | 写入代表文件系统支持用户磁盘配额,默认不支持                  |
| prpquota      | 写入代表文件系统支持组磁盘配额,默认不支持                    |
|               |                                                              |

```shell
[root@localhost /]# mount -o remount,noexec /home
#重新挂载/boot分区,并使用noexec权限
[root@localhost /]# cd /home
[root@localhost home]# vim hello.sh
[root@localhost home]# chmod 755 hello.sh 
[root@localhost home]# ./hello.sh
-bash: ./hello.sh: 权限不够
[root@localhost home]# mount -o remount,exec /home
#记得改回来啊,要不会影响系统启动的
```

### 9.2.3 挂载光盘和U盘

#### 9.2.3.1 挂载光盘

[root@localhost ~]# mkdir /mnt/cdrom/

#建立挂载点

[root@localhost ~]# mount -t ios9660 /dev/cdrom/ /mnt/cdrom/

#挂载光盘



[root@localhost ~]# mount /dev/sro /mnt/cdrom/

#### 9.2.3.2 卸载命令

[root@localhost ~]#  umount 设备文件名 或挂载点

[root@localhost ~]#  umount /mnt/cdrom



#### 9.2.3.3 挂载U盘

[root@localhost ~]# fdisk -l

#查看U盘设备文件名

[root@localhost ~]# mount -t vfat /dev/sdbl /mnt/usb/

注意: Linux默认是不支持NTFS文件系统的

> 

### 9.2.4 支持NTFS文件系统

#### 9.2.4.1 下载NTFS-3G插件

http://www.tuxera.com/community/ntfs-3g-download/

![image-20201001002428927](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201001002428927.png)



#### 9.2.4.3 使用



[root@localhost ~]#  mount -t ntfs-3g 分区设备文件名 挂载点



## 9.3 fdisk分区

### 9.3.1 fdisk命令分区过程



#### 9.3.1.1添加新硬盘

![image-20201001003648203](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201001003648203.png)



#### 9.3.1.2 查看新硬盘

[root@localhost ~]#  fdisk -l

#### 9.3.1.3 使用fdisk命令分区


[root@localhost ~]#  fdisk /dev/sdb

![image-20201001004508484](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201001004508484.png)

#### 9.3.1.4 重新读取分区表信息

[root@localhost ~]#  partprobe

#### 9.3.1.5 格式化分区

[root@localhost ~]#  mkfs -t ext4 /dev/sdb1

#### 9.3.1.6 建立挂载点并挂载

[root@localhost ~]#  mkdir /disk1

[root@localhost ~]#   mount /dev/sdb1 /disk1/

![image-20201001010116921](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201001010116921.png)

### 9.3.2 自动挂载与fstab文件修复

#### 9.3.2.1  /etc/fstab文件

- 第一字段 : 分区设备文件名或UUID ( 硬盘通用唯一识别码 )

- 第二字段 : 挂载点

- 第三字段 : 文件系统名称

- 第四字段 : 挂载参数 

- 第五字段 : 指定分区是否被dump备份 , 0代表不备份 , 1代表每天备份 , 2代表不定期备份

- 第六字段 : 指定分区是否被fsck检测 , 0代表不检测 , 其他数字代表检测的优先级 , 那么当然1的优先级比2高

#### 9.3.2.2 分区自动挂载

[root@localhost ~]# vim /etc/fstab

加一行

/dev/sdb1               /disk1                  ext4    defaults        1 2

[root@localhost ~]#  mount -a

#依据配置文件 /etc/fstab的内容,自动挂载

#### 9.3.2.3  /etc/fstab文件修复

[root@localhost ~]# mount -o remount,rw /



## 9.4 分配swap分区

### 9.4.1 free命令

[root@localhost ~]#  free

#查看内存与swap分区使用状况

- cached( 缓存) : 是指把读取出来的数据保存在内在当中,当再次读取时,不用读取硬盘而直接从内存当中读取,加速了数据的读取过程

- buffer( 缓冲) : 是指在写入数据时 , 先把分散的写入操作保存到内存当中 , 当达到一定程度再集中写入硬盘 , 减少了磁盘碎片和硬盘的反复寻道 , 加速了数据的写入过程

### 9.4.2 新建swap分区

[root@localhost ~]#  fdisk /dev/sdb

别忘记把分区ID改为82

### 9.4.3 格式化

[root@localhost ~]#  mkswap /dev/sdb6



### 9.4.4 加入swap 分区

[root@localhost ~]#  swapon /dev/sdb6

#加入swap分区

[root@localhost ~]#  swapoff /dev/sdb6

#取消swap分区

### 9.4.5 swap分区开机自动挂载

[root@localhost ~]#  vi/etc/fstab

加一行

/dev/sdb6               swap                    swap    defaults        0 0



[root@localhost ~]#  mount -a

#依据配置文件 /etc/fstab的内容,自动挂载



# 10. `Shell`基础

## 10.1 `Shell`概述

> 

## 10.1.1 `Shell`是什么

- `Shell`是一个命令行解释器,它为用户提供了一个向`Linux`内核发送请求以便运行程序的界面系统级程序,用户可以用`Shell`来启动、挂起、停止甚至是编写一些程序 .

![image-20201001020139403](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201001020139403.png)

- `Shell`还是一个功能相当强大的编程语言 , 易编写 , 易调试 , 灵活性较强 . `Shell`是解释执行的脚本语言,在`Shell`中可以直接调用`Linux`系统命令 .

> 

### 10.1.2 `Shell`的分类

- Bourne `Shell` : 从1979起Unix就开始使用

  Bourne `Shell `: Bourne `Shell` 主文件名为sh

- C `Shell` : C `Shell`主要在BSD版的Unix系统中使用 , 其语法和C语言相类似而得名
- `Shell`的两种主要语法类型有Bourne和C,这两种语法彼此不兼容 . Bourne家族主要包括sh、ksh、Bash、psh、zsh;C家族主要包括:csh、tcsh
- Bash : Bash和sh兼容,现在使用的Linux就是使用Bash作为用户的基本Shell .

> 

### 10.1.3 Linux支持的`Shell`

- /etc/shells

## 10.2 `Shell脚本`的执行方式

> 

### 10.2.1 echo输出命令

[root@localhost ~]# ehco [选项] [输出内容]

选项:

​			-e:			支持反斜线控制的字符转换

| 控制字符 | 作用                                                         |
| -------- | ------------------------------------------------------------ |
| \ \      | 输出\本身                                                    |
| \a       | 输出警告音                                                   |
| \b       | 退格键,也就是左删除键                                        |
| \c       | 取消输出行末的换行符 . 和“-n”选项一致.                       |
| \e       | ESCAPE键                                                     |
| \f       | 换页符                                                       |
| \n       | 换行符                                                       |
| \r       | 回车键                                                       |
| \t       | 制表符,也就是tab键                                           |
| \v       | 垂直制表符                                                   |
| \0nnn    | 按照八进制ASCII码表输出字符 . 其中0为数字零,nnn是三位八进制数 |
| \xhh     | 按照十八进制ASCII码表输出字符. 其中hh是两位十六进制数        |

[root@localhost ~]# echo -e “ab\bc”

#删除左侧字符

```shell
[root@localhost ~]# echo -e "a\tb\tc\nd\te\tf"
```



#制表符与换行符

![image-20201001031906165](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201001031906165.png)

```shell
 echo -e "\x61\t\x62\t\x63\n\x64\t\x65\t\x66"
```

```shell
 echo -e "\e[1;31m abcd \e[0m"
```

​	#输出颜色

​	#30m=黑色,31m=红色,32m=绿色,33m=黄色

​	#34m=蓝色,35m=洋红,36m=青色,37m=白色

> 

### 10.2.2 第一个`Shell`脚本

```shell
[root@localhost sh]# vim hello.sh
#!/bin/bash
#The first program
#Author : LiuQuan (E-mail:1515817@qq.com)

echo -e "Mr.Liu Quan is the most honest man in LampBrother"
```

> 

### 10.2.3 脚本执行

- 赋予执行权限,直接运行
  - chmod 755 hello.sh
  - ./hello.sh
- 通过bash调用执行脚本
  -  bash hello.sh

### 用Shell实现俄罗斯方块代码(Tetris.sh)

```shell
#!/bin/bash

# Tetris Game
# 10.21.2003 xhchen<[email]xhchen@winbond.com.tw[/email]>

#APP declaration
APP_NAME="${0##*[\\/]}"
APP_VERSION="1.0"


#颜色定义
cRed=1
cGreen=2
cYellow=3
cBlue=4
cFuchsia=5
cCyan=6
cWhite=7
colorTable=($cRed $cGreen $cYellow $cBlue $cFuchsia $cCyan $cWhite)

#位置和大小
iLeft=3
iTop=2
((iTrayLeft = iLeft + 2))
((iTrayTop = iTop + 1))
((iTrayWidth = 10))
((iTrayHeight = 15))

#颜色设置
cBorder=$cGreen
cScore=$cFuchsia
cScoreValue=$cCyan

#控制信号
#改游戏使用两个进程，一个用于接收输入，一个用于游戏流程和显示界面;
#当前者接收到上下左右等按键时，通过向后者发送signal的方式通知后者。
sigRotate=25
sigLeft=26
sigRight=27
sigDown=28
sigAllDown=29
sigExit=30

#七中不同的方块的定义
#通过旋转，每种方块的显示的样式可能有几种
box0=(0 0 0 1 1 0 1 1)
box1=(0 2 1 2 2 2 3 2 1 0 1 1 1 2 1 3)
box2=(0 0 0 1 1 1 1 2 0 1 1 0 1 1 2 0)
box3=(0 1 0 2 1 0 1 1 0 0 1 0 1 1 2 1)
box4=(0 1 0 2 1 1 2 1 1 0 1 1 1 2 2 2 0 1 1 1 2 0 2 1 0 0 1 0 1 1 1 2)
box5=(0 1 1 1 2 1 2 2 1 0 1 1 1 2 2 0 0 0 0 1 1 1 2 1 0 2 1 0 1 1 1 2)
box6=(0 1 1 1 1 2 2 1 1 0 1 1 1 2 2 1 0 1 1 0 1 1 2 1 0 1 1 0 1 1 1 2)
#所有其中方块的定义都放到box变量中
box=(${box0[@]} ${box1[@]} ${box2[@]} ${box3[@]} ${box4[@]} ${box5[@]} ${box6[@]})
#各种方块旋转后可能的样式数目
countBox=(1 2 2 2 4 4 4)
#各种方块再box数组中的偏移
offsetBox=(0 1 3 5 7 11 15)

#每提高一个速度级需要积累的分数
iScoreEachLevel=50        #be greater than 7

#运行时数据
sig=0                #接收到的signal
iScore=0        #总分
iLevel=0        #速度级
boxNew=()        #新下落的方块的位置定义
cBoxNew=0        #新下落的方块的颜色
iBoxNewType=0        #新下落的方块的种类
iBoxNewRotate=0        #新下落的方块的旋转角度
boxCur=()        #当前方块的位置定义
cBoxCur=0        #当前方块的颜色
iBoxCurType=0        #当前方块的种类
iBoxCurRotate=0        #当前方块的旋转角度
boxCurX=-1        #当前方块的x坐标位置
boxCurY=-1        #当前方块的y坐标位置
iMap=()                #背景方块图表

#初始化所有背景方块为-1, 表示没有方块
for ((i = 0; i < iTrayHeight * iTrayWidth; i++)); do iMap[$i]=-1; done


#接收输入的进程的主函数
function RunAsKeyReceiver()
{
        local pidDisplayer key aKey sig cESC sTTY

        pidDisplayer=$1
        aKey=(0 0 0)

        cESC=`echo -ne "\033"`
        cSpace=`echo -ne "\040"`

        #保存终端属性。在read -s读取终端键时，终端的属性会被暂时改变。
        #如果在read -s时程序被不幸杀掉，可能会导致终端混乱，
        #需要在程序退出时恢复终端属性。
        sTTY=`stty -g`

        #捕捉退出信号
        trap "MyExit;" INT TERM
        trap "MyExitNoSub;" $sigExit

        #隐藏光标
        echo -ne "\033[?25l"


        while :
        do
                #读取输入。注-s不回显，-n读到一个字符立即返回
                read -s -n 1 key

                aKey[0]=${aKey[1]}
                aKey[1]=${aKey[2]}
                aKey[2]=$key
                sig=0

                #判断输入了何种键
                if [[ $key == $cESC && ${aKey[1]} == $cESC ]]
                then
                        #ESC键
                        MyExit
                elif [[ ${aKey[0]} == $cESC && ${aKey[1]} == "[" ]]
                then
                        if [[ $key == "A" ]]; then sig=$sigRotate        #<向上键>
                        elif [[ $key == "B" ]]; then sig=$sigDown        #<向下键>
                        elif [[ $key == "D" ]]; then sig=$sigLeft        #<向左键>
                        elif [[ $key == "C" ]]; then sig=$sigRight        #<向右键>
                        fi
                elif [[ $key == "W" || $key == "w" ]]; then sig=$sigRotate        #W, w
                elif [[ $key == "S" || $key == "s" ]]; then sig=$sigDown        #S, s
                elif [[ $key == "A" || $key == "a" ]]; then sig=$sigLeft        #A, a
                elif [[ $key == "D" || $key == "d" ]]; then sig=$sigRight        #D, d
                elif [[ "[$key]" == "[]" ]]; then sig=$sigAllDown        #空格键
                elif [[ $key == "Q" || $key == "q" ]]                        #Q, q
                then
                        MyExit
                fi

                if [[ $sig != 0 ]]
                then
                        #向另一进程发送消息
                        kill -$sig $pidDisplayer
                fi
        done
}

#退出前的恢复
function MyExitNoSub()
{
        local y

        #恢复终端属性
        stty $sTTY
        ((y = iTop + iTrayHeight + 4))

        #显示光标
        echo -e "\033[?25h\033[${y};0H"
        exit
}


function MyExit()
{
        #通知显示进程需要退出
        kill -$sigExit $pidDisplayer

        MyExitNoSub
}


#处理显示和游戏流程的主函数
function RunAsDisplayer()
{
        local sigThis
        InitDraw

        #挂载各种信号的处理函数
        trap "sig=$sigRotate;" $sigRotate
        trap "sig=$sigLeft;" $sigLeft
        trap "sig=$sigRight;" $sigRight
        trap "sig=$sigDown;" $sigDown
        trap "sig=$sigAllDown;" $sigAllDown
        trap "ShowExit;" $sigExit

        while :
        do
                #根据当前的速度级iLevel不同，设定相应的循环的次数
                for ((i = 0; i < 21 - iLevel; i++))
                do
                        sleep 0.02
                        sigThis=$sig
                        sig=0

                        #根据sig变量判断是否接受到相应的信号
                        if ((sigThis == sigRotate)); then BoxRotate;        #旋转
                        elif ((sigThis == sigLeft)); then BoxLeft;        #左移一列
                        elif ((sigThis == sigRight)); then BoxRight;        #右移一列
                        elif ((sigThis == sigDown)); then BoxDown;        #下落一行
                        elif ((sigThis == sigAllDown)); then BoxAllDown;        #下落到底
                        fi
                done
                #kill -$sigDown $$
                BoxDown        #下落一行
        done
}


#BoxMove(y, x), 测试是否可以把移动中的方块移到(x, y)的位置, 返回0则可以, 1不可以
function BoxMove()
{
        local j i x y xTest yTest
        yTest=$1
        xTest=$2
        for ((j = 0; j < 8; j += 2))
        do
                ((i = j + 1))
                ((y = ${boxCur[$j]} + yTest))
                ((x = ${boxCur[$i]} + xTest))
                if (( y < 0 || y >= iTrayHeight || x < 0 || x >= iTrayWidth))
                then
                        #撞到墙壁了
                        return 1
                fi
                if ((${iMap[y * iTrayWidth + x]} != -1 ))
                then
                        #撞到其他已经存在的方块了
                        return 1
                fi
        done
        return 0;
}


#将当前移动中的方块放到背景方块中去,
#并计算新的分数和速度级。(即一次方块落到底部)
function Box2Map()
{
        local j i x y xp yp line

        #将当前移动中的方块放到背景方块中去
        for ((j = 0; j < 8; j += 2))
        do
                ((i = j + 1))
                ((y = ${boxCur[$j]} + boxCurY))
                ((x = ${boxCur[$i]} + boxCurX))
                ((i = y * iTrayWidth + x))
                iMap[$i]=$cBoxCur
        done

        #消去可被消去的行
        line=0
        for ((j = 0; j < iTrayWidth * iTrayHeight; j += iTrayWidth))
        do
                for ((i = j + iTrayWidth - 1; i >= j; i--))
                do
                        if ((${iMap[$i]} == -1)); then break; fi
                done
                if ((i >= j)); then continue; fi

                ((line++))
                for ((i = j - 1; i >= 0; i--))
                do
                        ((x = i + iTrayWidth))
                        iMap[$x]=${iMap[$i]}
                done
                for ((i = 0; i < iTrayWidth; i++))
                do
                        iMap[$i]=-1
                done
        done

        if ((line == 0)); then return; fi

        #根据消去的行数line计算分数和速度级
        ((x = iLeft + iTrayWidth * 2 + 7))
        ((y = iTop + 11))
        ((iScore += line * 2 - 1))
        #显示新的分数
        echo -ne "\033[1m\033[3${cScoreValue}m\033[${y};${x}H${iScore}         "
        if ((iScore % iScoreEachLevel < line * 2 - 1))
        then
                if ((iLevel < 20))
                then
                        ((iLevel++))
                        ((y = iTop + 14))
                        #显示新的速度级
                        echo -ne "\033[3${cScoreValue}m\033[${y};${x}H${iLevel}        "
                fi
        fi
        echo -ne "\033[0m"


        #重新显示背景方块
        for ((y = 0; y < iTrayHeight; y++))
        do
                ((yp = y + iTrayTop + 1))
                ((xp = iTrayLeft + 1))
                ((i = y * iTrayWidth))
                echo -ne "\033[${yp};${xp}H"
                for ((x = 0; x < iTrayWidth; x++))
                do
                        ((j = i + x))
                        if ((${iMap[$j]} == -1))
                        then
                                echo -ne "  "
                        else
                                echo -ne "\033[1m\033[7m\033[3${iMap[$j]}m\033[4${iMap[$j]}m[]\033[0m"
                        fi
                done
        done
}


#下落一行
function BoxDown()
{
        local y s
        ((y = boxCurY + 1))        #新的y坐标
        if BoxMove $y $boxCurX        #测试是否可以下落一行
        then
                s="`DrawCurBox 0`"        #将旧的方块抹去
                ((boxCurY = y))
                s="$s`DrawCurBox 1`"        #显示新的下落后方块
                echo -ne $s
        else
                #走到这儿, 如果不能下落了
                Box2Map                #将当前移动中的方块贴到背景方块中
                RandomBox        #产生新的方块
        fi
}

#左移一列
function BoxLeft()
{
        local x s
        ((x = boxCurX - 1))
        if BoxMove $boxCurY $x
        then
                s=`DrawCurBox 0`
                ((boxCurX = x))
                s=$s`DrawCurBox 1`
                echo -ne $s
        fi
}

#右移一列
function BoxRight()
{
        local x s
        ((x = boxCurX + 1))
        if BoxMove $boxCurY $x
        then
                s=`DrawCurBox 0`
                ((boxCurX = x))
                s=$s`DrawCurBox 1`
                echo -ne $s
        fi
}


#下落到底
function BoxAllDown()
{
        local k j i x y iDown s
        iDown=$iTrayHeight

        #计算一共需要下落多少行
        for ((j = 0; j < 8; j += 2))
        do
                ((i = j + 1))
                ((y = ${boxCur[$j]} + boxCurY))
                ((x = ${boxCur[$i]} + boxCurX))
                for ((k = y + 1; k < iTrayHeight; k++))
                do
                        ((i = k * iTrayWidth + x))
                        if (( ${iMap[$i]} != -1)); then break; fi
                done
                ((k -= y + 1))
                if (( $iDown > $k )); then iDown=$k; fi
        done

        s=`DrawCurBox 0`        #将旧的方块抹去
        ((boxCurY += iDown))
        s=$s`DrawCurBox 1`        #显示新的下落后的方块
        echo -ne $s
        Box2Map                #将当前移动中的方块贴到背景方块中
        RandomBox        #产生新的方块
}


#旋转方块
function BoxRotate()
{
        local iCount iTestRotate boxTest j i s
        iCount=${countBox[$iBoxCurType]}        #当前的方块经旋转可以产生的样式的数目

        #计算旋转后的新的样式
        ((iTestRotate = iBoxCurRotate + 1))
        if ((iTestRotate >= iCount))
        then
                ((iTestRotate = 0))
        fi

        #更新到新的样式, 保存老的样式(但不显示)
        for ((j = 0, i = (${offsetBox[$iBoxCurType]} + $iTestRotate) * 8; j < 8; j++, i++))
        do
                boxTest[$j]=${boxCur[$j]}
                boxCur[$j]=${box[$i]}
        done

        if BoxMove $boxCurY $boxCurX        #测试旋转后是否有空间放的下
        then
                #抹去旧的方块
                for ((j = 0; j < 8; j++))
                do
                        boxCur[$j]=${boxTest[$j]}
                done
                s=`DrawCurBox 0`

                #画上新的方块
                for ((j = 0, i = (${offsetBox[$iBoxCurType]} + $iTestRotate) * 8; j < 8; j++, i++))
                do
                        boxCur[$j]=${box[$i]}
                done
                s=$s`DrawCurBox 1`
                echo -ne $s
                iBoxCurRotate=$iTestRotate
        else
                #不能旋转，还是继续使用老的样式
                for ((j = 0; j < 8; j++))
                do
                        boxCur[$j]=${boxTest[$j]}
                done
        fi
}


#DrawCurBox(bDraw), 绘制当前移动中的方块, bDraw为1, 画上, bDraw为0, 抹去方块。
function DrawCurBox()
{
        local i j t bDraw sBox s
        bDraw=$1

        s=""
        if (( bDraw == 0 ))
        then
                sBox="\040\040"
        else
                sBox="[]"
                s=$s"\033[1m\033[7m\033[3${cBoxCur}m\033[4${cBoxCur}m"
        fi

        for ((j = 0; j < 8; j += 2))
        do
                ((i = iTrayTop + 1 + ${boxCur[$j]} + boxCurY))
                ((t = iTrayLeft + 1 + 2 * (boxCurX + ${boxCur[$j + 1]})))
                #\033[y;xH, 光标到(x, y)处
                s=$s"\033[${i};${t}H${sBox}"
        done
        s=$s"\033[0m"
        echo -n $s
}


#更新新的方块
function RandomBox()
{
        local i j t

        #更新当前移动的方块
        iBoxCurType=${iBoxNewType}
        iBoxCurRotate=${iBoxNewRotate}
        cBoxCur=${cBoxNew}
        for ((j = 0; j < ${#boxNew[@]}; j++))
        do
                boxCur[$j]=${boxNew[$j]}
        done


        #显示当前移动的方块
        if (( ${#boxCur[@]} == 8 ))
        then
                #计算当前方块该从顶端哪一行"冒"出来
                for ((j = 0, t = 4; j < 8; j += 2))
                do
                        if ((${boxCur[$j]} < t)); then t=${boxCur[$j]}; fi
                done
                ((boxCurY = -t))
                for ((j = 1, i = -4, t = 20; j < 8; j += 2))
                do
                        if ((${boxCur[$j]} > i)); then i=${boxCur[$j]}; fi
                        if ((${boxCur[$j]} < t)); then t=${boxCur[$j]}; fi
                done
                ((boxCurX = (iTrayWidth - 1 - i - t) / 2))

                #显示当前移动的方块
                echo -ne `DrawCurBox 1`

                #如果方块一出来就没处放，Game over!
                if ! BoxMove $boxCurY $boxCurX
                then
                        kill -$sigExit ${PPID}
                        ShowExit
                fi
        fi



        #清除右边预显示的方块
        for ((j = 0; j < 4; j++))
        do
                ((i = iTop + 1 + j))
                ((t = iLeft + 2 * iTrayWidth + 7))
                echo -ne "\033[${i};${t}H        "
        done

        #随机产生新的方块
        ((iBoxNewType = RANDOM % ${#offsetBox[@]}))
        ((iBoxNewRotate = RANDOM % ${countBox[$iBoxNewType]}))
        for ((j = 0, i = (${offsetBox[$iBoxNewType]} + $iBoxNewRotate) * 8; j < 8; j++, i++))
        do
                boxNew[$j]=${box[$i]};
        done

        ((cBoxNew = ${colorTable[RANDOM % ${#colorTable[@]}]}))

        #显示右边预显示的方块
        echo -ne "\033[1m\033[7m\033[3${cBoxNew}m\033[4${cBoxNew}m"
        for ((j = 0; j < 8; j += 2))
        do
                ((i = iTop + 1 + ${boxNew[$j]}))
                ((t = iLeft + 2 * iTrayWidth + 7 + 2 * ${boxNew[$j + 1]}))
                echo -ne "\033[${i};${t}H[]"
        done
        echo -ne "\033[0m"
}


#初始绘制
function InitDraw()
{
        clear
        RandomBox        #随机产生方块，这时右边预显示窗口中有方快了
        RandomBox        #再随机产生方块，右边预显示窗口中的方块被更新，原先的方块将开始下落
        local i t1 t2 t3

        #显示边框
        echo -ne "\033[1m"
        echo -ne "\033[3${cBorder}m\033[4${cBorder}m"

        ((t2 = iLeft + 1))
        ((t3 = iLeft + iTrayWidth * 2 + 3))
        for ((i = 0; i < iTrayHeight; i++))
        do
                ((t1 = i + iTop + 2))
                echo -ne "\033[${t1};${t2}H||"
                echo -ne "\033[${t1};${t3}H||"
        done

        ((t2 = iTop + iTrayHeight + 2))
        for ((i = 0; i < iTrayWidth + 2; i++))
        do
                ((t1 = i * 2 + iLeft + 1))
                echo -ne "\033[${iTrayTop};${t1}H=="
                echo -ne "\033[${t2};${t1}H=="
        done
        echo -ne "\033[0m"


        #显示"Score"和"Level"字样
        echo -ne "\033[1m"
        ((t1 = iLeft + iTrayWidth * 2 + 7))
        ((t2 = iTop + 10))
        echo -ne "\033[3${cScore}m\033[${t2};${t1}HScore"
        ((t2 = iTop + 11))
        echo -ne "\033[3${cScoreValue}m\033[${t2};${t1}H${iScore}"
        ((t2 = iTop + 13))
        echo -ne "\033[3${cScore}m\033[${t2};${t1}HLevel"
        ((t2 = iTop + 14))
        echo -ne "\033[3${cScoreValue}m\033[${t2};${t1}H${iLevel}"
        echo -ne "\033[0m"
}


#退出时显示GameOVer!
function ShowExit()
{
        local y
        ((y = iTrayHeight + iTrayTop + 3))
        echo -e "\033[${y};0HGameOver!\033[0m"
        exit
}


#显示用法.
function Usage
{
        cat << EOF
Usage: $APP_NAME
Start tetris game.

  -h, --help              display this help and exit
      --version           output version information and exit
EOF
}


#游戏主程序在这儿开始.
if [[ "$1" == "-h" || "$1" == "--help" ]]; then
        Usage
elif [[ "$1" == "--version" ]]; then
        echo "$APP_NAME $APP_VERSION"
elif [[ "$1" == "--show" ]]; then
        #当发现具有参数--show时，运行显示函数
        RunAsDisplayer
else
        bash $0 --show&        #以参数--show将本程序再运行一遍
        RunAsKeyReceiver $!        #以上一行产生的进程的进程号作为参数
fi
```

![image-20201001035324151](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201001035324151.png)

> 

## 10.3 `Bash`的基本功能

### 10.3.1 历史命令和与命令补全

#### 10.3.1.1 历史命令

[root@localhost ~]# history  [选项] [历史命令保存文件]

选项 :

​			-c: 		清空历史命令

​			-w:		把缓存中的历史命令写入历史命令保存文件	~/.bash_history

- 历史命令默认会保存1000条,可以在环境变量配置文件/etc/profile中进行修改

> 历史命令的调用

- 使用上、下箭头调用以前的历史命令

- 使用“!n”重复执行第n条历史命令

- 使用“!!” 重复执行上一条命令

- 使用“!字串”重要执行最后一条以该字串开头的命令

#### 10.3.1.2 命令与文件补全

- 在Bash中,命令与文件补全是非常方便与常用的功能,我们只要在输入命令或文件时,按“Tab”键就会自动进行补全

### 10.3.2 命令别名与常用快捷键

#### 10.3.2.1 命令别名

[root@localhost ~]# alias	别名=‘原命令’

#设定命令别名

[root@localhost ~]#alias

#查询命令别名

> 命令执行时顺序

1 第一顺位执行用绝对路径或相对路径执行的命令.

2 第二顺位执行别名 .

3 第三顺位执行Bash的内部命令 .

4 第四顺位执行按照 $ PATH 环境变量定义的目录查找顺序找到的第一个命令 .

> 让别名永久生效

[root@localhost ~]# vim /root/.bashrc

> 删除别名

[root@localhost ~]# unalias 别名

#### 10.3.2.2 Bash常用 快捷键

| 快捷键 | 使用                                                         |
| ------ | ------------------------------------------------------------ |
| ctrl+A | 把光标移动到命令行开头 . 如果我们的输入命令过长,想要把光标移动到命令行开头时使用. |
| ctrl+E | 把光标移动到命令行结尾 .                                     |
| ctrl+C | 强制终止当前的命令 .                                         |
| ctrl+L | 清屏 , 相当于clean命令 .                                     |
| ctrl+U | 删除或剪切光标之前的命令 . 我输入了一行很长的命令 ,不用使用退格键一个一个字符的删除 , 使用这个快捷键会更加方便 . |
| ctrl+K | 删除或剪切光标之后的内容 .                                   |
| ctrl+Y | 粘贴 Ctrl+U 或Ctrl+K 剪切的内容 .                            |
| ctrl+R | 在历史命令中搜索,按下CTRL+R之后,就会出现搜索界面,只要输入搜索内容,就会从历史命令中搜索. |
| ctrl+D | 退出当前终端 .                                               |
| ctrl+Z | 暂停 ,并放入后台 . 这个快捷键牵扯工作管理的内容 , 我们在每户管理章节详细介绍 . |
| ctrl+S | 暂停屏幕输出                                                 |
| ctrl+Q | 恢复屏幕输出                                                 |

### 10.3.3 输入输出重定向

#### 10.3.3.1 标准输入输出

| 设备   | 设备文件名  | 文件描述符 | 类型         |
| ------ | ----------- | ---------- | ------------ |
| 键盘   | /dev/stbin  | 0          | 标准输入     |
| 显示器 | /dev/sdtout | 1          | 标准输出     |
| 显示器 | /dev/sdterr | 2          | 标准错误输出 |

#### 10.3.3.2 输出重定向

![image-20201002220649881](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201002220649881.png)

![image-20201002221533088](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201002221533088.png)

#### 10.3.3.3 输入重定向

[root@localhost ~]# wc [选项] [文件名]

选项:

​			-c		统计定节数

​			-w 	 统计单词数

​			-l		 统计行数

命令<文件		把文件作为命令的输入

> 

### 10.3.4 多命令顺序执行与管道符

#### 10.3.4.1 多命令顺序执行

| 多命令执行符 | 格式             | 作用                                                         |
| ------------ | ---------------- | ------------------------------------------------------------ |
| ;            | 命令1 ；命令2    | 多个命令顺序执行,命令之间没有任何逻辑联系                    |
| &&           | 命令1 && 命令2   | 逻辑与<br />当命令1正确执行,则命令2才会执行<br />当命令1执行不正确,则命令2不会执行 |
| \|\|         | 命令1 \|\| 命令2 | 逻辑或<br />当命令1执行不正确,则命令2才会执行<br />当命令1正确执行,则命令2不会执行 |

例子:

[root@localhost ~]# ls ; date ; cd /user ; pwd



[root@localhost ~]#  dd if =输入文件 of =输出文件 bs=字节数  count=个数

选项:

​			if=输入文件					指定源文件或源设备

​			of=输出文件				  指定目标文件或目标设备

​			bs=字节数					  指定一次输入/输出多少字节,即把这些字节看做一个数据块

​			count=个数				   指定输入/输出多少个数据块

例子:

```shell
[root@localhost ~]# date ; dd if=/dev/zero of=/root/testfile bs=1k count=100000 ; date
[root@localhost ~]# ls anaconda-ks.cfg && echo yes
[root@localhost ~]# ls /root/test || echo "no"
[root@localhost ~]# 命令 && echo yes || echo no
```

> 

#### 10.3.4.2	管道符

命令格式:

```shell
[root@localhost ~]# 命令1 |命令2
```

#命令1的正确输出作为命令2的操作对象

颜色显示

例子:

```shell
[root@localhost ~]# ll -a /etc/ |more
[root@localhost ~]# netstat -an |grep "ESTABLISHED"
```

[root@localhost ~]# grep [选项] “搜索内容” 文件名

选项:

​			-i:			忽略大小写

​			-n:			输出行号

​			-v:			反向查找

​			--color=auto		搜索出的关键字用颜色显示

> 

### 10.3.5 通配符与其他特殊符号

#### 10.3.5.1 通配符

| 通配符 | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| ？     | 匹配一个任意字符                                             |
| *      | 匹配0个或任意多个任意字符,也就是可以匹配任何内容             |
| []     | 匹配中括号中任意一个字符 . 例如: [abc]代表一定匹配一个字符,或者是a,或者是b,或者是c . |
| [-]    | 匹配中括号中任意一个字符, - 代表一个范围 . 例如 :[a-z] 代表一个小写字母 . |
| [^]    | 逻辑非,表示匹配不是中括号的一个字符 . 例如 : [ ^ 0-9] 代表匹配一个不是数字的字符 . |

![image-20201002231955791](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201002231955791.png)

####  10.3.5.2 Bash 中其他特殊符号

| 符号 | 作用                                                         |
| ---- | ------------------------------------------------------------ |
| ‘’   | 单引号 . 在单引号中所有的特殊符号 , 如 “$” 和 “ `” (反引号)都没有特殊含义 . |
| “”   | 双引号 . 在双引号中特殊符号都没有特殊含义,但是“$”、“`”和“\”是例外,拥有“调用变量的值”、“引用命令”和“转义符”的特殊含义. |
| ``   | 反引号 . 反引号括起来的内容是系统命令 , 在Bash中会先执行它 . 和$()作用一样,不过推荐使用  \$(), 因为反引号非常容易看错 . |
| $()  | 和反引号作用一样,用来引用系统命令 .                          |
| #    | 在Shell脚本中 ,#开头的行代表注释 .                           |
| $    | 用于调用变量的值 , 如需要调用变量 name 的值时 , 需要用$name的方式得到变量的值 . |
| \    | 转义符 , 跟在\之后的特殊符号将失去特殊含义 , 变为普通字符 .<br />如\\$将输出 “\$”符号,而不当做是变量引用 . |

> 

## 10.4 `Bash`的变量

### 10.4.1 用户自定义变量

> 

#### 10.4.1.1 什么是变量

- 变量是计算机内存的单元,其中存放的值可以改变.当`Shell`脚本需要保存一些信息时,如一个文件名或是一个数字,就把它存放在一个变量中 . 每个数量有一个名字,所以很容易引用它 . 使用变量可以保存有用信息 , 使系统获知用户相关设置 , 变量也可以用于保存暂时信息 .

#### 10.4.1.2 

- 变量名称可以由字母、数字和下划线组成,但是不能以数字开头 . 如果变量名是“2name”则是错误的 .

- 在Bash中,变量的默认类型都是字符串型,如果要进行数值运算,则必修指定变量类型为数值型 .
- 变量用等号连接值,等号左右两侧不能有空格 .
- 变量的值如果有空格 , 需要使用单引号或双引号包括 .
- 在变量的值中 , 可以使用 “ \ ”转义符 .
- 如果需要增加变量的值,那么可以进行变量值的叠加 . 不过变量需要用双引号包含 “ $变量名”或用\${变量名}包含 
- 如果是把命令的结果作为变量值赋予变量 , 则需要使用反引号或 $() 包含命令 .
- 环境变量名建议大写 , 便于区分 .

#### 10.4.1.3 变量分类

- 用户自定义数量

- 环境变量 : 这种变量中主要保存的是和系统操作环境相关的数据 .

- 位置参数变量 : 这种变量主要是用来向脚本当中传递参数或数据的 , 变量名不能自定义 , 变量作用是固定的 .

- 预定义数量 : 是Bash中已经定义好的变量 , 变量名不能自定义 , 变量作用也是固定的 .

#### 10.4.1.4 本地变量

- 变量定义

```shell
[root@localhost ~]# name="shen chao"
```

- 变量增加

```shell
[root@localhost ~]# aa=123
[root@localhost ~]# aa="$aa"456
[root@localhost ~]# aa=${aa}789
```

- 变量调用

```shell
[root@localhost ~]# echo $name
```

- 变量查看

```shell
[root@localhost ~]# set
```

- 变量删除

```shell
[root@localhost ~]# unset name
```

> 

### 10.4.2 环境变量

#### 10.4.2.1 环境变量是什么

- 用户自定义变量只在当前的`Shell`中生效,而环境变量会在当前`Shell`和这个`Shell`的所有子`Shell`当中生效 . 如果把环境变量写入相应的配置文件 , 那么这个环境变量就会在所有的`Shell` 中生效 .

#### 10.4.2.2 设置环境变量

export 变量名=变量值

#申请变量



env

#查询变量



unset 变量名

#删除变量

- #### 系统常见环境变量

PATH : 系统查找命令的路径 

[root@localhost ~]# echo $PATH

/usr/lib64/qt-3.3/bin:/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin

PATH=“$PATH”:/root/sh

#PATH变量叠加

- PS1 : 定义系统提示符的变量

  \d:	显示日期,格式为 “ 星期   月   日”

  \h:	显示简写主机名 . 如默认主机名 “localhost”

  \t: 	显示24小时制时间 , 格式 为 “HH:MM:SS”

  \T:	显示12小时制时间,格式为“HH:MM:SS”

  \A:	显示24小时制时间,格式为“HH:MM”

  \u:	显示当前用户名

  \w:	显示当前所在目录的完整名称

  \W:	显示当前所在目录的最后一个目录

  \\#:	执行的第几个命令

  \\$:	提示符 . 如果是root用户会显示提示符为“#” , 如果是普通用户会是显示提示符为 “\$”

举例:

```shell
[root@localhost ~]# PS1='[\u@\t \w]\$'
[root@18:59:00 ~]#echo $PS1
[\u@\t \w]\$
[root@18:59:32 ~]#PS1=[\u@\h \W]\$
-bash: W]$: command not found
[root@19:00:37 ~]# PS1='[\u@\h \W]\$'
[root@localhost ~]#
```

> 

### 10.4.3 位置参数变量

#### 10.4.3.1 位置参数变量

| 位置参数变量 | 作用                                                         |
| ------------ | ------------------------------------------------------------ |
| $n           | n为数字,$0代表命令本身,\$1-\$9代表第一到第九个参数,十以上的参数需要用大括号包含,如\$｛10｝ |
| $*           | 这个变量代表命令行中所有的参数,$*把所有的参数看成一个整体    |
| $@           | 这个变量也代表命令行中所有的参数 , 不过$@把每个参数区分对待  |
| $#           | 这个变量代表命令行中所有参数的个数                           |

例子1:

#!/bin/bash

num1=$1

num2=$2

sum=$((\$sum1+\$sum2))

#变量sum的和是num1加num2

echo $sum

#打印变量sum的值

![image-20201003010734237](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003010734237.png)

![image-20201003010755852](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003010755852.png)



例子2:

#!/bin/bash

echo “A total of $# parameters”

#使用$#代表所有参数的个数

echo “The paramenter is : $*”

#使用S*代表所有的参数

echo “The parameters is : $@”

#使用$@也代表所有参数

![image-20201003011329005](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003011329005.png)



例子3 : $*与\$@的区别

#!/bin/bash

for i in “($*)”

#$*中的所有参数看成是一个整体,所以这个for循环只会循环一次

​	do

​			echo “The	parameters is : $i”

​	done



x=1

for y in “$@”

#$@中的每个参数都看成独立的,所以“\$@” 中有几个参数,就会循环几次

​	do

​			echo “The parameter$x is :\$y”

​			x=$((\$+1))

​	done

![image-20201003012019620](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003012019620.png)



![image-20201003012027316](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003012027316.png)

> 

### 10.4.4 预定义定量

#### 10.4.4.1 预定义定量

| 预定义变量 | 作用                                                         |
| ---------- | ------------------------------------------------------------ |
| $?         | 最后一次执行的命令的返回状态 . 如果这个变量的值为0 , 证明上一个命令正确执行；如果这个变量的值为非0(具体是哪个数,由命令自己来决定) , 则证明上一个命令执行不正确了. |
| $$         | 当前进程的进程号(PID)                                        |
| $!         | 后台运行的最后一个进程的进程号(PID)                          |

#!/bin/bash

#Author : thenchao ( E-mail : shenchao@lampbrother.net)

echo “The current process is $$”

#输出当前进程的PID .

#这个PID就是variable.sh 这个脚本执行时 , 生成的进程的PID



find /root-name hello.sh &

#使用find 命令 在root目录下查找 hello.sh文件

#符号&的意思把命令放入后台执行,工作管理我们在系统管理章节会详细介绍

echo “The lase one Daemon process is $!”



#### 10.4.4.2 接收键盘输入

[root@localhost ~]# read [选项] [变量名]

选项:

​		-p “提示信息”:	在等待read输入时 , 输出提示信息

​		-t	秒数:				 read命令会一直等待用户输入,使用此选项可以指定等待时间

​		-n	字符数:		   read命令只接受指定的字符数,就会执行

​		-s:							   隐藏输入的数据,适用于机密信息的输入



#!/bin/bash

#Author : shenchao ( E-mail : shenchao@lampbrother.net)

read -t 30 -p “please input your name:” name

#提示 “请输入姓名”并等待30秒,把用户的输入保存入变量name中

echo “Name is $name”



read -s -t 30 -p “Please enter your age”: age

#年龄是隐私,所以我们用“-s”选项隐藏输入

echo -e “\n”

echo “Age is $age”





read -n l -t 30 -p “Please select your gender[M/F]:” gender

#使用“-n l” 选项只接收一个输入字符就会执行(都不用输入回车)

echo -e “\n”

echo “Sex is $gender”

> 

## 10.5 `Bash`运算符

### 10.5.1 数值运算与运算符

#### 10.5.1.1 declare声明变量类型

[root@localhost ~]# declare [+/-] [选项] 变量名

选项:

​			-:			给变量设定类型属性

​			+:			取消变量的类型属性

​			-i:			将变量声明为整数型( integer )

​			-x:			将变量声明为环境变量

​			-p:			显示指定变量的被声明的类型

#### 10.5.1.2 数值运算

方法1

[root@localhost ~]#  aa=11

[root@localhost ~]#  bb=22

#给变量aa和bb赋值

[root@localhost ~]# declare -i cc=$aa+\$bb

方法2: expr或let 数值运算工具

[root@localhost ~]# aa=11

[root@localhost ~]# bb=22

#给变量aa和bb赋值

[root@localhost ~]#  dd=$(expr  \$aa + \$bb)

#dd的值是aa和bb的和 . 注意“+”号左右两侧必须有空格

![image-20201003025059421](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003025059421.png)



方法3: “$((运算式))”或“\$[运算式]”

[root@localhost ~]# aa=11

[root@localhost ~]# bb=22

[root@localhost ~]# ff=$((\$aa+\$bb))

[root@localhost ~]# gg=$[\$aa+\$bb]

#### 10.4.4.3 运算符

![image-20201003025625629](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003025625629.png)

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003025944440.png)

### 10.5.2 变量测试与内容替换

| 变量置换方式 | 变量y没有设置                    | 变量y为空值            | 变量y设置值       |
| ------------ | -------------------------------- | ---------------------- | ----------------- |
| x=${y-新值}  | x=新值                           | x为空                  | x=$y              |
| x=${y:-新值} | x=新值                           | x=新值                 | x=$y              |
| x=${y+新值}  | x为空                            | x=新值                 | x=新值            |
| x=${y:+新值} | x为空                            | x为空                  | x=新值            |
| x=${y=新值}  | x=新值<br />y=新值               | x为空<br />y值不变     | x=$y<br />y值不变 |
| x=${y:=新值} | x=新值<br />y=新值               | x=新值<br />y=新值     | x=$y<br />y值不变 |
| x=${y?新值}  | 新值输出到标准错误输出(就是屏幕) | x为空                  | x=$y              |
| x=${y:?新值} | 新值输出到标准错误输出           | 新值输出到标准错误输出 | x=$y              |

![image-20201003031306012](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003031306012.png)

> 

## 10.6 环境变量配置文件

### 10.6.1 环境变量配置文件简单介

#### 10.6.1.1 `source 命令

[root@localhost ~]# source 配置文件

或

[root@localhost ~]# . 配置文件

#### 10.6.1.2 环境变量配置文件简介

- 环境变量配置文件中主要是定义对系统的操作环境生效的系统默认环境变量,比如PATH、HISTSIZE、PS1、HOSTNAME等默认环境变量.
- /etc/profile
- /etc/profile.d/*.sh
- ~/.bash_profile
- ~/bashrc
- /etc/bashrc

> 

### 10.6.2 环境变量配置文件作用



![image-20201003034733009](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003034733009.png)

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003035336996.png)

/etc/profile的作用 : 

- USER变量:
- LOGNAME变量:
- MAIL变量:
- HOSTNAME变量:
- HISTSIZE变量:
- umask:
- 调用/etc/profie.d/*.sh文件

![image-20201003040213163](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003040213163.png)

~/.bash_profile的作用

- 调用了~/.bashrc文件 .
- 在PATH变量后面加入了“ :$HOME/bin ”这个目录

![image-20201003040349552](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003040349552.png)

~/.bashrc的作用

- 主要保存bai个人的一些个性化设置，du如命令别名、路径等(定义默认别名),
- 个人建议可以加alias grep='grep --color=auto' 这一行,这个命令挺常用
- 调用/etc/bashrc



![image-20201003040955574](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003040955574.png)

/etc/bashrc的使用

- PS1变量
- umask
- PATH变量
- 调用 /etc/profile.d/*.sh文件

> 

### 10.6.3 其他配置文件和登录信息

#### 10.6.3.1 注销时生效的环境变量配置文件

- ~/.bash_logout

#### 10.6.3.2 其他配置文件

- ~/.bash_history

#### 10.6.3.3 Shell登录信息

- 本地终端欢迎信息: /etc/issue

| 转义符 | 作用                            |
| ------ | ------------------------------- |
| \d     | 显示当前系统日期                |
| \s     | 显示操作系统名称                |
| \l     | 显示登录的终端号,这个比较常用   |
| \m     | 显示硬件体系结构,如i386、i686等 |
| \n     | 显示主机名                      |
| \o     | 显示域名                        |
| \r     | 显示内核版本                    |
| \t     | 显示当前系统时间                |
| \u     | 显示当前系统用户的序列号        |

- 远程终端欢迎信息: /etc/issue.net
  - 转义符在/etc/issue.net文件中不能使用
  - 是否显示此欢迎信息,由ssh的配置文件/etc/ssh/sshd_config决定,加入“Banner/etc/issue.net”行才能显示(记得重启SSH服务)

- 登录后欢迎信息 : /etc/motd

不管是本地登录,还是远程登录,都可以显示此欢迎信息

> 

# 11. `Shell`编程

## 11.1 基础正则表达式

###  11.1.1 正则表达式与通配符

- 正则表达式用来在文件中匹配符合条件的字符串,正则是[包含匹配][] .` grep`、 `awk`、`sed`等命令可以支持正则表达式 .
- 通配符用来匹配符合条件的文件名 , 通配符是[完全匹配][] . `ls`、`find`、`cp`这些命令不支持正则表达式,所以只能使用shell自己的通朽符进行匹配了.

#### 11.1.2 基础正则表达式

![image-20201003044954070](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003044954070.png)

![image-20201003045650841](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003045650841.png)

![image-20201003045727605](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003045727605.png)

![image-20201003045950552](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003045950552.png)



![image-20201003050009136](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003050009136.png)



![image-20201003050112556](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003050112556.png)



![image-20201003050210968](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003050210968.png)



![image-20201003050247836](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003050247836.png)



![image-20201003050403742](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003050403742.png)

> 

## 11.2 字符截取命令

### 11.2.1 cut字段提取命令

[root@localhost ~]# cut [选项] 文件名

选项:

​			-f 列号 : 							提取第几列

​			-d 分隔符 :					   按照指定分隔符分割列



[root@localhost ~]# vim student.txt



![image-20201003051909522](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003051909522.png)

```shell
[root@localhost ~]# cat /etc/passwd
root:x:0:0:root:/root:/bin/bash
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
adm:x:3:4:adm:/var/adm:/sbin/nologin
lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
sync:x:5:0:sync:/sbin:/bin/sync
shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
halt:x:7:0:halt:/sbin:/sbin/halt
mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
uucp:x:10:14:uucp:/var/spool/uucp:/sbin/nologin
operator:x:11:0:operator:/root:/sbin/nologin
games:x:12:100:games:/usr/games:/sbin/nologin
gopher:x:13:30:gopher:/var/gopher:/sbin/nologin
ftp:x:14:50:FTP User:/var/ftp:/sbin/nologin
nobody:x:99:99:Nobody:/:/sbin/nologin
dbus:x:81:81:System message bus:/:/sbin/nologin
vcsa:x:69:69:virtual console memory owner:/dev:/sbin/nologin
rpc:x:32:32:Rpcbind Daemon:/var/cache/rpcbind:/sbin/nologin
abrt:x:173:173::/etc/abrt:/sbin/nologin
haldaemon:x:68:68:HAL daemon:/:/sbin/nologin
ntp:x:38:38::/etc/ntp:/sbin/nologin
saslauth:x:499:76:"Saslauthd user":/var/empty/saslauth:/sbin/nologin
postfix:x:89:89::/var/spool/postfix:/sbin/nologin
avahi:x:70:70:Avahi mDNS/DNS-SD Stack:/var/run/avahi-daemon:/sbin/nologin
rpcuser:x:29:29:RPC Service User:/var/lib/nfs:/sbin/nologin
nfsnobody:x:65534:65534:Anonymous NFS User:/var/lib/nfs:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
tcpdump:x:72:72::/:/sbin/nologin
oprofile:x:16:16:Special user account to be used by OProfile:/home/oprofile:/sbin/nologin
weqq01:x:500:500::/home/weqq01:/bin/bash
weqq02:x:501:501::/home/weqq02:/bin/bash
sc:x:550:550:test user:/home/lamp1:/bin/bash
weqq001:x:551:551::/home/weqq001:/bin/bash
weqq002:x:552:552::/home/weqq002:/bin/bash
weqq003:x:553:553::/home/weqq003:/bin/bash
st:x:554:555::/home/st:/bin/bash
[root@localhost ~]# cat /etc/passwd | grep /bin/bash
root:x:0:0:root:/root:/bin/bash
weqq01:x:500:500::/home/weqq01:/bin/bash
weqq02:x:501:501::/home/weqq02:/bin/bash
sc:x:550:550:test user:/home/lamp1:/bin/bash
weqq001:x:551:551::/home/weqq001:/bin/bash
weqq002:x:552:552::/home/weqq002:/bin/bash
weqq003:x:553:553::/home/weqq003:/bin/bash
st:x:554:555::/home/st:/bin/bash
[root@localhost ~]# cat /etc/passwd | grep /bin/bash |grep -v root
weqq01:x:500:500::/home/weqq01:/bin/bash
weqq02:x:501:501::/home/weqq02:/bin/bash
sc:x:550:550:test user:/home/lamp1:/bin/bash
weqq001:x:551:551::/home/weqq001:/bin/bash
weqq002:x:552:552::/home/weqq002:/bin/bash
weqq003:x:553:553::/home/weqq003:/bin/bash
st:x:554:555::/home/st:/bin/bash
[root@localhost ~]# cat /etc/passwd | grep /bin/bash | grep -v root
weqq01:x:500:500::/home/weqq01:/bin/bash
weqq02:x:501:501::/home/weqq02:/bin/bash
sc:x:550:550:test user:/home/lamp1:/bin/bash
weqq001:x:551:551::/home/weqq001:/bin/bash
weqq002:x:552:552::/home/weqq002:/bin/bash
weqq003:x:553:553::/home/weqq003:/bin/bash
st:x:554:555::/home/st:/bin/bash
[root@localhost ~]# cat /etc/passwd | grep /bin/bash | grep -v root |cut -d ":" -f 1
weqq01
weqq02
sc
weqq001
weqq002
weqq003
st

```

> cut命令的局限

[root@localhost ~]# df -h |cut -d “ ” -f 1,3

### 11.2.2 printf命令

printf ‘输出类型输出格式’ 输出内容

输出类型:

​					%ns:					输出字符串 . n 是数字指代输出几个字符

​					%ni:					 输出整数 . n是数字指代输出几个数字

​					%m.nf:     	    输出浮点数 . m 和 n 是数字,指代输出的整数位数和小数位数 . 如%8.2f代表共输出8位数,其	

​													中2位是小数,6位是整数.

![image-20201003053753001](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003053753001.png)



![image-20201003053835245](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003053835245.png)



![image-20201003054452596](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003054452596.png)



在awk命令的输出中支持print和printf命令

- print: 	print会在每个输出之后自动加入一个换行符(Linux默认没有print命令)
- printf:	printf是标准格式输出命令,并不会自动加入换行符,如果需要换行,需要手工加入换行符

> 

### 11.2.3 awk命令

#awk ‘条件1｛动作1｝条件2｛动作2｝...’ 文件名

条件(pattern):

​		一般使用关系表达式作为条件

​		x>10				判断变量x是否大于10

​		x>=10			 大于等于

​		x<=10			 小于等于

动作	(Action):

​		格式化输出

​		流程控制语句

![image-20201003055406333](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003055406333.png)

![image-20201003055902228](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003055902228.png)



>  BEGIN

```shell
awk 'BEGIN {printf "This is a transcript\n"}{printf $2 "\t" $6 "\n"}' student.txt
```

![image-20201003060347373](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003060347373.png)

> FS内置变量

```shell
cat /etc/passwd | grep "/bin/bash" | awk 'BEGIN {FS=":"}{printf $1 "\t" $3 "\n"}'
```

![image-20201003060818455](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003060818455.png)



![image-20201003060903993](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003060903993.png)

> END

```shell
awk 'END{printf"The End\n"}{printf $2 "\t" $6 "\n"}' student.txt
```

> 关系运算符

cat student.txt |grep -v Name | awk ‘$6>=87 {printf $2 “\n”’

### 11.2.4 sed命令

> sed 命令

`sed`是一种几乎包括在所有UNIX平台(包括Linux)的轻量级流编辑器 . sed主要是用来将数据进行选取、替换、删除、新增的命令 .

[root@localhost ~]#  sed [选项] ‘[动作]’ 文件名

选项:

​		-n:			一般sed命令会把所有数据都输出到屏幕 , 如果加入此选择 , 则只会把经过sed命令处理的行输出屏幕

​		-e:			允许对输入数据应用多条sed命令编辑

​		-i:			 用sed的修改结果直接修改读取数据的文件,而不是由屏幕输出

动作:

​		a\:			追加,在当前行后添加一行或多行 . 添加多行时,除最后一行外,每行未尾需要用“\”代表数据未完结 .

​		c\:			行替换,用c后面的字符串替换原数据行,替换多行时,除最后一行外,每行未尾需用“\”代表数据未完结.

​		i\:			 插入,在当期行前插入一行或多行 . 插入多行时 , 除最后一行外,每行未尾需要用“\”代表数据未完结.

​		d:			 删除,删除指定的行 .

​		p:			 打印,输出指定的行 .

​		s:			 字距替换 , 用一个字符串替换另外一个字符串 . 格式为“行范围 s/ 旧字串/新字串/g”(和vim中的替换格式						 类似)

> 行数据操作

[root@localhost ~]# sed ‘2p’ student.txt

#查看文件的第二行

[root@localhost ~]#  sed -n ‘2p’ student.txt



[root@localhost ~]# sed ‘2,4d’ student.txt

#删除第二行到第四行数据,但不修改文件本身



[root@localhost ~]# sed ‘2a hello’  student.txt

#在第二行后追加hello



[root@localhost ~]# sed ‘2i hello ]

world’ student.txt

#在第二行前插入两行数据



[root@localhost ~]#  sed ‘2c No such person’ student.txt

#数据替换

> 字符串替换

[root@localhost ~]#  sed ‘s/旧字串/新字串/g’ 文件名



[root@localhost ~]# sed ‘3s/74/99/g’ student.txt

#第三行中,把74换成99

[root@localhost ~]# sed -i ‘3s/74/99/g’ student.txt

#sed操作的数据直接写入文件



[root@localhost ~]# sed -e’s/Liming//g ; s/Gao//g’ student.txt

#同时把“Liming”和“Gao”替换为空

## 11.3 字符处理命令

### 11.3.1 排序命令

[root@localhost ~]# sort [选项] 文件名

选项:

​			-f:			忽略大小写

​			-n:			以数值型进行排序,默认使用字符串排序

​			-r:			 反向排序

​			-t:			 指定分隔符,默认是分隔符是制表符

​			-k n[,m]:	按照指定的字段范围排序 . 从第n字段开始 , m字段结束 ( 默认到行尾 )



[root@localhost ~]# sort /etc/passwd

#排序用户信息文件



[root@localhost ~]#  sort -r /etc/passwd

#反向排序



[root@localhost ~]# sort -r  “:” -k 3,3 /etc/passwd

#指定分隔符是“:” , 用第三字段开头,第三字段结尾排序,就是只用第三字段排序

### 11.3.2 统计命令wc

[root@localhost ~]# wc [选项] 文件名

选项:

​		-l:				只统计行数

​		-w:			 只统计单词数

​		-m:			 只统计字符数



## 11.4 条件判断

### 11.4.1 按照文件类型进行判断

| 测试选项 | 作用                                                         |
| -------- | ------------------------------------------------------------ |
| -b 文件  | 判断该 文件是否存在,并且是否块设备文件(是块设备文件为真)     |
| -c 文件  | 判断该文件是否存在,并且是否为字符设备文件(是字符设备文件为真) |
| -d 文件  | 判断该文件是否存在,并且是否为目录文件(是目录是真)            |
| -e 文件  | 判断该文件是否存在(存在为真)                                 |
| -f 文件  | 判断该文件是否存在,并且是否为普遍文件 (是普遍文件为真)       |
| -L 文件  | 判断该文件是否存在,并且是否是符号链接文件(符号链接文件为真)  |
| -p 文件  | 判断该文件是否存在,并且是否为管道文件(是管道文件为真)        |
| -s 文件  | 判断该文件是否存在,并且是否为非空 (非空为真)                 |
| -S 文件  | 判断该文件是否存在,并且是否为套接字文件 ( 套接字文件为真)    |

两种判断格式

[root@localhost ~]# test -e /root/install.log

[root@localhost ~]# [ -e /root/install.log ]

[root@localhost ~]# [ -d /root ] && echo “yes” || echo “no”

#第一个判断命令如果正确执行,则打印“yes”,否则打印“no”

![image-20201007070507107](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007070507107.png)

### 11.4.2 按照文件权限进行判断

| 测试选项 | 作用                                                         |
| -------- | ------------------------------------------------------------ |
| -r 文件  | 判断该文件是否存在,并且是否该文件拥有读权限(有读权限为真)    |
| -w 文件  | 判断该文件是否存在,并且是否该文件拥有写权限(有写权限为真)    |
| -x 文件  | 判断该文件是否存在,并且是否该文件拥有执行权限(有执行权限为真) |
| -u 文件  | 判断该文件是否存在,并且是否该文件拥有SUID权限(有SUID权限为傎) |
| -g 文件  | 判断该文件是否存在,并且是否该文件拥有SGID权限(有SGID权限为真) |
| -k 文件  | 判断该文件是否存在,并且是否该文件拥有SBit权限(有Sbit权限为真) |

### 11.4.3 两个文件之间进行比较

| 测试选项        | 作用                                                         |
| --------------- | ------------------------------------------------------------ |
| 文件1 -nt 文件2 | 判断文件1的修改时间是否比文件2的新(如果新则为真)             |
| 文件1 -ot 文件2 | 判断文件1的修改时间是否比文件2的旧(如果旧则为真)             |
| 文件1 -ef 文件2 | 判断文件1是否和文件2的Inode号一致 , 可以理解为两个文件是否为同一个文件 . 这个判断用于判断硬链接是很好的方法 |

[root@localhost ~]#  ln /root/student.txt /tmp/stu.txt

[root@localhost ~]#  [ /root/student.txt -ef /tmp/stu.txt ] && echo “yes” || echo “no”

#用test测试下,果然很有用

### 11.4.4 两个整数之间比较

| 测试选项        | 作用                                   |
| --------------- | -------------------------------------- |
| 整数1 -eq 整数2 | 判断整数1是否和整数2相等(相等为真)     |
| 整数1 -ne 整数2 | 判断整数1是否和整数2不相等(不相等为真) |
| 整数1 -gt 整数2 | 判断整数1是否和整数2(大于为真)         |
| 整数1 -lt 整数2 | 判断整数1是否和整数2(小于为真)         |
| 整数1 -ge 整数2 | 判断整数1是否和整数2(大于等于为真)     |
| 整数1 -le 整数2 | 判断整数1是否和整数2(小于等于为真)     |

### 11.4.5 字符串的判断

| 测试选项        | 作用                                         |
| --------------- | -------------------------------------------- |
| -z 字符串       | 判断字符串是否为空(为空返回真)               |
| -n 字符串       | 判断字符串是否为非空(非空返回真)             |
| 字串1 == 字串2  | 判断字符串1是否和字符串2相等(相等返回真)     |
| 字串1 ！= 字串2 | 判断字符串1是否和字符串2不相等(不相等返回真) |

name=sc

#给name变量赋值

[ -z “$name” ] && echo “yes” || echo “no”

no

#判断name变量是否为空,因为不为空,所以返回no

### 11.4.6 多重条件判断

| 测试选项       | 作用                                           |
| -------------- | ---------------------------------------------- |
| 判断1 -a 判断2 | 逻辑与,判断1和判断2都成立,最终的结果才是真     |
| 判断1 -o 判断2 | 逻辑或,判断1和判断2有一个成立,最终的结果就为真 |
| ! 判断         | 逻辑非,使原始的判断式取反                      |

> 

## 11.5 流程控制

### 11.5.1 if语句

#### 11.5.1.1 单分支if条件语句

if [ 条件判断式 ]; then

​	程序

fi

或者

if [ 条件判断式]

​	then

​			程序

fi

> 单分支条件语句需要注意几个点

- if语句使用fi结尾,和一般语言使用大括号结尾不同
- [ 条件判断式 ] 就是使用test命令判断,所以中括号和条件判断式这间必须有空格
- then后面跟符合条件之后执行的程序,可以放在[]之后,用“;”分割.也可以换行写入,就不需要“;”了.

> 例子: 判断分区使用率

```shell
#! /bin/bash
#统计根分区使用率
#authoer: weqq (E-mail:1515817@qq.com)



rate=$(df -h | grep "/dev/sda5" | awk '{print $5}' | cut -d "%" -f1)

#把根分区使用率作为变量值赋予变量rate

if [ $rate -ge 80 ]

        then
                echo “Warning! /dev/sda3 is full!!!”

fi

```



![image-20201007081051079](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007081051079.png)

#### 11.5.1.2 双分支if 条件语句

if [ 条件判断式]

​	then

​				条件成立时,执行的程序

​	else

​				条件不成立时,执行的另一个程序

fi

> 例子1:备份mysql数据库

```shell
#!/bin/bash
#备份mysql数据库
#Author: weqq (E-mail:1515817@qq.com)

ntpdate asia.pool.ntp.org &>/dev/null
#同步系统时间
date=$( date +%y%m%d)
#把当前系统时间按照 "年月日"格式赋予变量date
size=$( du -sh /etc)
#统计mysql数据库大小,并把大小赋予size变量.
if [ -d /tmp/dbbak ]
        then
                echo "Date: $date!" > /tmp/dbbak/dbinfo.txt
                echo "Data size : $size" >> /tmp/dbbak/dbinfo.txt
                cd /tmp/dbbak
                tar -zcf etc_$date.tar.gz /etc dbinfo.txt &>/dev/null
                rm -rf /tmp/dbbak/dbinfo.txt
        else
                mkdir /tmp/dbbak
                echo "Date: $date!" > /tmp/dbbak/dbinfo.txt
                echo "Data size : $size" >> /tmp/dbbak/dbinfo.txt
                cd /tmp/dbbak
                tar -zcf etc_$date.tar.gz /etc dbinfo.txt &>/dev/null
                rm -rf /tmp/dbbak/dbinfo.txt

fi

```

> 例子2:判断apache是否启动

```shell
#!/bin/bash

port=$(nmap -sT 192.168.0.188 | grep tcp | grep http | awk '{print $2}')
#使用nmap命令扫描服务器,并截取apache服务的状态,赋予变量port
if [ "$port" == "open" ]
        then
                echo "$(date) httpd is OK!" >>/tmp/autostart-acc.log
        else
                /etc/rc.d/init.d/httpd start &> /dev/null
                echo "$(date) restart httpd!!" >> /tmp/autostart-err.log
fi

```

![image-20201007103128239](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007103128239.png)

![image-20201007103617665](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007103617665.png)

#### 11.5.1.3 多分支if条件语句

if [ 条件判断式1 ]

​	then

​				当条件判断式1成立时,执行程序1

elif	[ 条件判断式2 ]

​	then

​				当条件判断式2成立时,执行程序2

...省略更多条件...

else

​		当所有条件都不成立时,最后执行此程序

fi

```shell
#!/bin/bash
#判断用户输入的是什么文件

read -p "Please input a filename : " file
#接收键盘的输入,并赋予变量file

if [ -z "$file" ]
#判断file变量是否为空
    then
        echo "error , please input a filename"
        exit 1
elif [ ! -e "$file" ]
#判断file的值是否存在
    then
        echo "you input is not a file!"
        exit 2
elif [ -f "$file" ]
#判断file的值是否为普通文件
    then
        echo " $file is a regulare file!"
elif [ -d "$file" ]
#判断file的值是否为目录文件
    then 
        echo " $file is a directory!"
else
    echo " $file is an other file!"
fi

```

![image-20201007110219652](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007110219652.png)



### 11.5.2 case语句

> 多分支 case条件语句

- case语句和if...elif...else语句一样都是多分支条件语句,不过和if多分支条件语句不同的是,case语句只能判断一种条件关系,而if语句可以判断多种条件关系.

case $变量名 in

​		“值1”)

​					如果变量的值等于值1,则执行程序1

​					;;

​		“值2”)

​					如果变量的值等于值2,则执行程序2

​					;;

​		“值3”)

​					如果变量的值等于值3,则执行程序3

​					;;

​		...省略其他分支...

​		*)

​					如果变量的值都不是以上的值,则执行此程序

​					;;

esac

```shell
#!/bin/bash
#判断用户输入

read -p "Please choose yes/no:" -t 30 cho 
case $cho in  
    "yes")
            echo "Your choose is yes!"
            ;;  
    "no")
            echo "your choose is no!"
            ;;  
    *)  
            echo "your choose is error!"
            ;;  
esac

```

![image-20201007111255768](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007111255768.png)

### 11.5.3 for 循环

> 语法一

for 变量 in 值1 值2 值3 ...

​	do

​			程序

​	done

```shell
#!/bin/bash
#打印时间

for time in morning noon afternoon evening
    do  
        echo "This time is $time!"
    done

```

```shell
#!/bin/bash
#批量解压缩脚本

cd /root/sh

ls *.sh > ls.log

y=1
for i in $(cat ls.log)
    do  
        echo $y
        y=$(( $y+1 ))
        tar -zcf $i.tar.gz $i  &>/dev/null
    done
rm -rf ls.log

```

![image-20201007113758312](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007113758312.png)

> 语法 二

for ((初始值;循环控制条件;变量变化))

​	do

​		程序

​	done

```shell
#!/bin/bash
#从1加到100

s=0
for (( i=1;i<=100;i=i+1))
    do  
        s=$(( $s+$i ))
    done
echo "The sum of 1+2....+100 is : $s "
```

![image-20201007114706034](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007114706034.png)

```shell
#!/bin/bash
#批量添加指定数量的用户

read -p "Please input user name:" -t 30 name
read -p "Please input the number of users : " -t 30 num 
read -p "Please input the password of users:" -t 30 pass

if [ ! -z "$name" -a ! -z "$num" -a ! -z "$pass" ]
    then
    y=$( echo $num | sed 's/[0-9]//g')
    if [ -z "$y" ]
        then
        for (( i=1;i<=$num;i=i+1 ))
            do  
                /usr/sbin/useradd $name$i &> /dev/null
                echo $pass | /usr/bin/passwd --stdin $name$i &> /dev/null
            done
    fi  
fi

```

![image-20201007121456298](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007121456298.png)

![image-20201007121432229](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007121432229.png)



### 11.5.4 while循环与until循环

#### 11.5.4.1 while循环

- while 循环是不定循环 , 也称作条件循环 . 只要条件判断式成立 , 循环就会一直继续 , 直到条件判断式不成立,循环才会停止 . 这就和for 的固定循环不太一样了 .

while [ 条件判断式 ]

​	do

​		程序

​	done

```shell
#!/bin/bash
#从1加到100

i=1
s=0
while [ $i -le 100 ]
#如果变量i的值小于等于100,则执行循环
    do
        s=$(( $s+$i ))
        i=$(( $i+1 ))
    done
echo "the sum is : $s "

```

![image-20201007124032471](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007124032471.png)

#### 11.5.4.2 until循环

- until循环,和while循环相反,until循环时只要条件判断式不成立则进行循环,并执行循环程序 . 一旦循环条件成立 , 则终止循环 .

until [ 条件判断式 ]

​	do

​		程序

​	done



# 12. `Linux`服务管理

## 12.1 服务简介与分类

### 12.1.1 服务的分类

![image-20201007125543073](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201007125543073.png)

> 启动与自启动

- 服务启动: 就是在当前系统中让服务运行 , 并提供功能 .
- 服务自启动 : 自启动是指让服务在系统开机或重启动之后,随着系统的启动而自动启动服务 .

> 查询已安装的服务

- RPM包安装的服务

  - chkconfig --list

    #查看服务自启动状态 , 可以看到所有RPM包安装的服务

- 源码包安装的服务

  - 查看服务安装位置 , 一般是/usr/local的下

## 12.2 RPM包安装服务的管理

#### 12.2.1 独立服务的管理

#### 12.2.1.1 RPM安装服务和源码包安装服务的区别

- RPM安装服务和源码包安装服务的区别就是安装位置的不同
  - 源码包安装在指定位置,一般是/usr/local/
  - RPM包安装在默认位置中



- /etc/init.d/:										启动脚本位置
- /etc/sysconfig/:                         初始化环境配置文件位置
- /etc/:                                          配置文件位置
- /etc/xinetd.conf:                       xinetd配置文件
- /etc/xinetd.d/:                          基于xinted服务的启动脚本
- /var/lib/:                                   服务产生的数据放在这里
- /var/log/:                                  日志



#### 12.2.1.2 独立服务的启动

- /etc/init.d/ 独立服务名			start|stop|status|restart|



- service	独立服务名				start|stop|restart||status

#### 12.2.1.3 独立服务的自启动

- chkconfig [ --level 运行级别 ] [独立服务名] [on|off]
- 修改/etc/rc.d/rc.local文件
- 使用ntsysv命令管理自启动

### 12.2.2 基于xinetd服务管理

#### 12.2.2.1 安装xinetd与telnet

```shell
[root@localhost ~]# yum -y install xinetd
```

```shell
[root@localhost ~]# yum -y install telnet-server
```

#### 12.2.2.2 xinetd服务的启动

```shell
[root@localhost ~]#vim /etc/xinetd.d/telnet
```

service telnet																			服务的名称为telnet

{
    flags       = REUSE																标志为REUSE,设定TCP/IP socket 可重用
    socket_type = stream    												  使用TCP协议数据包
    wait        = no																		允许多个连接同时连接
    user        = root																	启动服务的用户为root
    server      = /usr/sbin/in.telnetd								  服务的启动程序
    log_on_failure  += USERID											登陆失败后,记录用户的ID
    disable     = `no` 																 服务不启动
}

重启xinetd服务

```shell
[root@localhost ~]# service xinetd restart
```

#### 12.2.2.3 xinetd服务的自启动

```shell
[root@localhost ~]# chkconfig telnet on
```

```shell 
ntsysv
```

## 12.3 源码包安装服务的管理

### 12.3.1 源码包安装服务的启动

- 使用绝对路径 , 调用启动脚本来启动 . 不同的源码包的启动脚本不同 . 可以查看源码包的安装说明 , 查看启动脚本的方法 .

  /usr/local/apache2/bin/apachectl	start|stop

### 12.3.2 源码包服务的自启动

```shell
[root@localhost ~]# vim /etc/rc.d/rc.local
```

加入

/usr/local/apache2/bin/apachectl start

### 12.3.3 让源码包服务被服务管理命令识别

- 让源码包的apache服务能被service命令管理启动

  ln -s /usr/local/apache2/bin/apachectl	/etc/init.d/apache

- 让源码包的apache服务能被chkconfig与ntsysv命令管理自启动

vim /etc/init.d/apache

#chkcofig: 35 86 76

#指定httpd脚本可以被chkconfig命令管理 . 格式是:

chkconfig : 运行级别 启动顺序 关闭顺序

#description: source package apache

#说明,内容随意

```shell
[root@localhost ~]# chkconfig --add apache
```

#把源码包apache加入chkconfig命令

# 13. 进程管理

## 13.1 进程管理

### 13.1.1 进程查看

#### 13.1.1.1 进程简介

- 进程是正在执行的一个程序或命令 , 每一个进程都是一个运行的实体 , 都有自己的地址空间 , 并占用一定的系统资源 .

#### 13.1.1.2 进程管理的作用

- 判断服务器健康状态
- 查看系统中所有进程
- 杀死进程

#### 13.1.1.3 查看系统中所有进程

```shell
[root@localhost ~]# ps aux
```

#查看系统中所有进程,使用BSD操作系统格式

```shell
[root@localhost ~]# ps -le
```

#查看系统中所有进程,使用Linux标准命令格式 

- USER:	该进程是由哪个用户产生的;

- PID:       进程的ID号;

- %CPU:  该进程占用CPU资源的百分比,占用越高,进程越耗费资源；

- %MEM:  该进程占用物理内存的百分比,占用越高,进程越耗费资源；

- VSZ:       该进程占用虚拟内存的大小,单位KB;

- RSS:       该进程占用实际物理内存的大小,单位KB;

- TTY:       该进程是在哪个终端中运行的 . 其中tty1-tty7代表本地控制台终端,tty1-tty6是本地的字符界面终端,tty7         

  ​              是图形终端 . pts/0-256代表虚拟终端 .
  
- STAT:     进程状态 . 常见的状态有: R : 运行 、S : 睡眠 、 T : 停止状态 、 s : 包含子进程 、 + : 位于后台
  
- START:   该进程的启动时间
  
- TIME:     该进程占用CPU的运算时间,注意不是系统时间
  
- COMMAND: 产生此进程的命令名

#### 13.1.1.4 查看系统健康状态

```shell
[root@localhost ~]# top	[选项]
```

选项:

​		-d 秒数:			指定top命令每隔几秒更新 . 默认是3秒

在top命令的交互模式当中可以执行的命令:

​	?或h:								显示交互模式的帮助

​	P:										以CPU使用率排序,默认就是此项

​	M:										以内存的使用率排序

​	N:										以PID排序

​	q:										退出top



> 第一行信息为任务队列信息

| 内容                               | 说明                                                         |
| ---------------------------------- | ------------------------------------------------------------ |
| 12:26:46                           | 系统当前时间                                                 |
| up 1 day , 13:32                   | 系统的运行时间,本机已经行动1天 13小时32分钟                  |
| 2 users                            | 当前登录了两个用户                                           |
| load average:    0.00,0.00,   0.00 | 系统在之前1分钟,5分钟,15分钟的平均负载 . 一般认为小于1时,负载较小 . 如果大于1,系统已经超出负荷. |

> 第二行为进程信息

| 内容           | 说明                                        |
| -------------- | ------------------------------------------- |
| Task: 95 total | 系统中的进程总数                            |
| 1 running      | 正在运行的进程数                            |
| 94 sleeping    | 睡眠的进程                                  |
| 0 stopped      | 正在停止的进程                              |
| 0 zombie       | 僵尸进程 . 如果不是0 , 需要手工检查僵尸进程 |

> 第三行 CPU信息

| 内容           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| Cpu(s): 0.1%us | 用户模式占用的CPU百分比                                      |
| 0.1%sy         | 系统模式占用的CPU百分比                                      |
| 0.0%ni         | 改变过优先级的用户进程占用的CPU百分比                        |
| 99.7%id        | 空闲的CPU的CPU百分比                                         |
| 0.1%wa         | 等待输入/输出的进程的占用CPU百分比                           |
| 0.0%hi         | 硬中断请求服务占用的CPU百分比                                |
| 0.1%si         | 软中断请求服务占用的CPU百分比                                |
| 0.0%st         | st(Steal time) 虚拟时间百分比 . 就是当有虚拟机时 , 虚拟CPU等待实际CPU的时间百分比 . |

> 第四行为物理内存信息

| 内容                    | 说明                                                         |
| ----------------------- | ------------------------------------------------------------ |
| Mem:     625344k  total | 物理内存的总量,单位KB                                        |
| 571504k   used          | 已经使用的物理内存数量                                       |
| 53840k   free           | 空闲的物理内存数量,我们使用的是虚拟机,总共只分配了628MB内存,所以只有53MB的空闲内存了 |
| 65800k   buffers        | 作为缓冲的内存数量                                           |

> 第五行为交换换分区( swap )信息

| 内容                     | 说明                          |
| ------------------------ | ----------------------------- |
| Swap :    524280k  total | 交换分区 ( 虚拟内存 )的总大小 |
| 0k   used                | 已经使用的交互分区的大小      |
| 524280k  free            | 空闲交换分区的大小            |
| 409280k  cached          | 作为缓存的交互分区的大小      |

#### 13.1.1.5查看进程树

```shell
[root@localhost ~]# pstree [选项]
选项:
	-p:			显示进程的PID
	-u:			显示进程的所属用户
```



### 13.1.2 进程管理

#### 13.1.2.1 Kill命令

```shell
[root@localhost ~]# kill -l
```

#查看可用的进程信号

| 信号代号 | 信号名称 | 说明                                                         |
| -------- | -------- | ------------------------------------------------------------ |
| 1        | SIGHUP   | 该信号让进程立即关闭,然后重新读取配置文件之后重启 .          |
| 2        | SIGINT   | 程序终止信号,用于终止前台进程 . 相当于输出ctrl+c快捷键 .     |
| 8        | SIGFPE   | 在发生致命的算术运算错误时发出 . 不仅包括浮点运算错误 , 还包括溢出及除数为0等其它所有的算术的错误 . |
| 9        | SIGKILL  | 用来立即结束程序的运行.本信号不能被阻塞、处理和忽略 .        |
| 14       | SIGALRM  | 时钟定时信号,计算的是实际的时间或时钟时间  . alarm函数使用该信号 |
| 15       | SIGTERM  | 正常结束进程的信号,kill命令的默认信号 . 有时如果进程已经发生问题 , 这个信号是无法正常终止进程的 , 我们才会尝试SIGKILL信号 , 也就是信号9 . |
| 18       | SIGCONT  | 该信号可以让暂停的进程恢复执行 , 本信号不能被阻断 .          |
| 19       | SIGSTOP  | 该信号可以暂停前台进程,相当于输入ctrl+z快捷键 . 本信号不能被阻断 . |

```shell
[root@localhost ~]# kill -1 22354
```

#重启进程

```shell
[root@localhost ~]# kill -9 23368
```

#强制杀死进程

#### 13.1.2.2 killall命令

```shell
[root@localhost ~]# killall [选项] [信号] 进程名
```

#按照进程名杀死进程

选项:

​		-i:				交互式,询问是否要杀死某个进程

​		-I:				忽略进程名的大小写

#### 13.1.2.3 pkill命令

```shell
[root@localhost ~]# pkill [选项] [信号] 进程名
```

#按照进程名终止进程

选项:

​		-t 终端号:				按照终端号踢出用户

> 按照终端号踢出用户

```shell
[root@localhost ~]# w
```

#使用w命令查询本机已经登录的用户

```shell
[root@localhost ~]# pkill -t -9 pts/1
```

#强制杀死从ps/1虚拟端登录的进程



## 13.2 工作管理

#### 13.2.1 把进程放入后台

- tar -zcf etc.tar.gz  /etc &

- [root@localhost ~]# top

  #在top命令执行的过程中,按下ctrl+z快捷键

#### 13.2.2 查看后台的工作

[root@localhost ~]#  jobs [-l]

选项:

​		-l:		显示工作的PID

注: “+” 号代表最近一个放入后台的工作,也是工作恢复时,默认恢复的工作. “-”号代表倒数第二个放入后台的工作

#### 13.2.3 将后台暂停的工作恢复到前台执行

[root@localhost ~]# fg %工作号

参数:

​		%工作号			%号可以省略,但是注意工作号和PID的区别

#### 13.2.4 把后台暂停的工作恢复到后台执行

[root@localhost ~]# bg %工作号

注:后台恢复执行的命令,是不能和前台有交互的,否则不能恢复到后台执行



## 13.3 系统资源查看



### 13.3.1 vmstat命令监控系统资源

[root@localhost ~]# vmstat [刷新延时 刷新次数]

例如:

```shell
[root@localhost ~]# vmstat 13
```

### 13.3.2 dmesg 开机时内核检测信息

[root@localhost ~]# dmesg

[root@localhost ~]# dmesg | grep CPU

### 13.3.3 free命令查看内存使用状态

[root@localhost ~]# free [ -b|-k|-m|-g]

选项:

​		-b:			以字节为单位显示

​		-k:			以KB为单位显示,默认就是以KB单位显示

​		-m:         以MB为单位显示

​		-g:			以GB为单位显示

> 缓存和缓冲的区别

- 简单来说缓存( cache )是用来加速数据从硬盘中“读取”的,而缓冲( buffer )是用来加速数据“写入”硬盘的.

### 13.3.4 查看CPU信息

[root@localhost ~]# cat /proc/cpuinfo

### 13.3.5 uptime命令

[root@localhost ~]# uptime

#显示系统的启动时间和平均负载,也就是top命令的第一行 . w命令也可以看到这个数据.

### 13.3.6 查看系统与内核相关信息

[root@localhost ~]# uname [选项]

选项:

​			-a:		查看系统所有相关信息；	

​			-r:		查看内核版本；

​			-s;		查看内核名称.

> 判断当前系统的位数

[root@localhost ~]# file /bin/ls 

[root@localhost ~]# uname -m

> 查询当前`Linux`系统的发行版本

```shell
[root@localhost ~]# lsb_release -a
```

### 13.3.7 列出进程打开或使用的文件信息

[root@localhost ~]# lsof [选项]

#列出进程调用或打开的文件的信息

选项:

​			-c  字符串:			只列出以字符串开头的进程打开的文件

​			-u  用户名:			只列出某个用户的进程打开的文件

​			-p  pid:					列出某个PID进程打开的文件

## 13.4 系统定时任务

### 13.4.1 crond服务管理与访问控制

```shell
[root@localhost ~]# service crond restart
```

```shell
[root@localhost ~]# chkconfig crond on
```

### 13.4.2 用户的crontab设置

[root@localhost ~]# crontab [选项]

选项:

​		-e:			编辑crontab定时任务

​		-l:			 查询crontab任务

​		-r:			 删除当前用户所有的crontab任务

```shell
[root@localhost ~]# crontab -e
```

#进入crontab编辑界面 . 会打开vim编辑你的工作.

```shell
*****执行的任务
```

| 项目      | 含义                 | 范围                      |
| --------- | -------------------- | ------------------------- |
| 第一个“*” | 一小时当中的第几分钟 | 0-59                      |
| 第二个“*” | 一天当中的第几小时   | 0-23                      |
| 第三个“*” | 一个月当中的第几天   | 1-31                      |
| 第四个“*” | 一年当中的第几月     | 1-12                      |
| 第五个“*” | 一周当中的星期几     | 0-7    (0和7都代表星期日) |

| 特殊符号 | 含义                                                         |
| -------- | ------------------------------------------------------------ |
| *        | 代表任何时间 . 比如第一个“*”就代表一小时中每分钟都执行一次的意思. |
| ,        | 代表不连续的时间 . 比如 “0 8 , 12,16 * * * 命令”,就代表在每天的8点0分,12点0分,16点0分都执行一次命令 |
| -        | 代表连续的时间范围.比如“0 5 * * 1-6命令” , 代表在周一到周六的凌晨5点0分执行命令 |
| */n      | 代表每隔多久执行一次.比如 “ */10 * * * * 命令”,代表每隔10分钟就执行一遍命令 |

| 时间              | 含义                                                         |
| ----------------- | ------------------------------------------------------------ |
| 45 22 * * * 命令  | 在22点45分钟执行命令                                         |
| 0 17 * * 1 命令   | 每周1的17点0分执行命令                                       |
| 0 5 1,15 * * 命令 | 每月1号和15号的凌晨5点0分执行命令                            |
| 40 4 * * 1-5 命令 | 每周一到周五的凌晨4点50分执行命令                            |
| */10 4 * * *命令  | 每天的凌晨4点,每隔10分钟执行一次命令                         |
| 0 0 1,15 * 1命令  | 每月1号和15号,每周1的0点0分都会执行命令.注意:星期几和几号最好不要同时出现,因为他们定义的都是天.非常容易让管理员混乱. |

> 举例

```shell
*/5 * * * * /bin/echo "11" >> /tmp/test

5 5 * * 2 /sbin/shutdown  -r now

0 5 1,10,15 * * /root/sh/autobak.sh
```

# 14. 日志管理

## 14.1 日志管理简介

### 14.1.1 日志服务

- 在CentOS 6.x 中日志服务已经由rsyslogd取代原先的syslogd服务.rsyslogd日志服务更加先进,功能更多.但是不论该服务的使用,还是日志文件的格式其实都是syslogd服务相兼容的,所以学习起来基本和syslogd服务一致.
- rsyslogd的新特点:
  - 基于TCP网络协议传输日志信息；
  - 更安全的网络传输方式；
  - 有日志消息的及时分析框架；
  - 后台数据库；
  - 配置文件中可以写简单的逻辑判断；
  - 与syslog配置文件相兼容.

> 确定服务启动

```shell
[root@localhost ~]# ps aux | grep rsyslogd
#查看服务是否启动

[root@localhost ~]# chkconfig --list | grep rsyslog
#查看服务是否自启动
```

![image-20201009104345291](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201009104345291.png)

### 14.1.2 常见日志的作用

| 日志文件         | 说明                                                         |
| ---------------- | ------------------------------------------------------------ |
| /var/log/cron    | 记录了系统定时任务相关的日志.                                |
| /var/log/cups/   | 记录打印信息的日志                                           |
| /var/log/dmesg   | 记录了系统在开机时内核自检的信息.也可以使用dmesg命令直接查看内核自检信息. |
| /var/log/btmp    | 记录错误登录的日志.这个文件是二进制文件,不能直接vi查看,而要使用lastb命令查看,命令如下:[root@localhost ~]#lastb<br />root tty1 Tue jun 4 22:38 - 22:38 (00-00)<br />#有人在6月4日22:38使用root用户,在本地终端1登录错误 |
| /var/log/lastlog | 记录系统中所有用户最后一次的登录时间的日志.这个文件也是二进制文件,不能直接vi,而要使用lastlog命令查看 |
| /var/log/mailog | 记录邮件信息 |
| /var/log/message | 记录系统重要信息的日志.这个日志文件中会记录Linux系统的绝大多数重要信息,如果系统出现问题时,首先要检查的就应该是这个日志文件. |
| /var/log/secure | 记录验证和授权方面的信息,只要涉及帐户和密码的程序都会记录.比如说系统的登录,ssh的登录,su切换用户,sudo授权,甚至添加用户和修改用户都会记录在这个日志文件中. |
| /var/log/wtmp | 永久记录所有用户的登录、注销信息,同时记录系统的启动、重启、关机事件.同样这个文件就是一个二进制文件,不能直接vi,而需要使用last命令来查看. |
| /var/run/utmp | 记录当前已经登录的用户的信息.这个文件会随着用户的登录和注销而不断变化,只记录当前登录用户的信息.同样这个文件不能直接vi,而要使用w,who,users等命令来查询. |

- 除了系统默认的日志之外,采用RPM方式安装的系统服务也会默认把日志记录在/var/log/目录中(源码包安装的服务日志是在源码包指定目录中) . 不过这些日志不是由rsyslogd服务来记录和管理的,而是各个服务使用自己的日志管理文档来记录自身日志.

| 日志文件        | 说明                                |
| --------------- | ----------------------------------- |
| /var/log/httpd/ | RPM包安装的apache服务的默认日志目录 |
| /var/log/mail/  | PRM包安装的邮件服务的额外日志目录   |
| /var/log/samba/ | RPM包安装的samba服务的日志目录      |
| /var/log/sssd/  | 守护进程安全服务目录                |

## 14.2 rsyslogd日志服务

### 14.2.1 日志文件格式

- 基于日志格式包含以下四列:
  - 事件产生的时间；
  - 发生事件的服务器的主机名；
  - 产生事件的服务名或程序名；
  - 事件的具体信息.

### 14.2.2 /etc/rsyslog.conf配置文件

authpriv.*				/var/log/secure

#服务名称[连接符号]日志等级							日志记录位置

#认证相关服务.所有日志等级							  记录在

​	/var/log/secure日志中

> 服务名称

| 服务名称      | 说明                                       |
| ------------- | ------------------------------------------ |
| auth          | 安全和认证相关消息(不推荐使用authpriv替代) |
| authpriv      | 安全和认证相关消息(私有的)                 |
| cron          | 系统定时任务cront和at产生的日志            |
| daemon        | 和各个守护进程相关的日志                   |
| ftp           | ftp守护进程产生的日志                      |
| kern          | 内核产生的日志(不是用户进程产生的)         |
| local0-local7 | 为本地使用预留的服务                       |
| lpr           | 打印产生的日志                             |
| mail | 邮件收信息 |
| news | 与新闻服务器相关的日志 |
| syslog | 有syslogd服务产生的日志信息(虽然服务名称已经改为rsyslogd,但是很多配置都还是沿用了syslogd的,这里并没有修改服务名) |
| user | 用户等级类别的日志信息 |
| uucp | uucp子系统的日志信息,uucp是早期linux系统进行数据传递的协议,后来也常用在新闻组服务中. |

> 连接符号

- 连接符号可以识别为:
  - “*”代表所有日志等级,比如:” authpriv.\* ” 代表 authpriv认证信息服务产生的日志,所有的日志等级都记录
  - “,”代表只要比后面的等级高的(包含该等级)日志都记录下来.比如:”cron.info”代表cron服务产生的日志,只要日志等级大于等于info级别,就记录
  - “.=”代表只记录所需等级的日志,其他等级的都不记录.比如:”*.=emerg”代表人和日志服务产生的日志,只要等级是emerg等级就记录.这种用法及少见,了解就好
  - “.!”代表不等于,也就是除了该等级的日志外,其他等级的日志都记录.

| 等级名称 | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| debug    | 一般的调试信息说明                                           |
| info     | 基本的通知信息                                               |
| notice   | 普通信息,但是有一定的重要性                                  |
| warning  | 警告信息,但是还不回影响到服务或系统运行                      |
| err      | 错误信息,一般达到err等级的信息以及可以影响到服务或系统的运行了. |
| crit     | 临界状况信息,比err等级还要严重                               |
| alert    | 警告状态信息,比crit还要严重.必须立即采取行动                 |
| emerg    | 疼痛等级信息,系统已经无法使用了.                             |

日志记录位置

- 日志文件的绝对路径,如“/var/log/secure”
- 系统设备文件,如“/dev/lp0”
- 转发给远程主机,如“@192.168.0.210:514”
- 用户名,如“root”
- 忽略或丢弃日志,如“~”


## 14.3 日志轮替

### 14.3.1 日志文件的命名规则

- 如果配置文件中拥有“dateext” 参数,那么日志会用日期来作为日志文件的后缀,例如“secure-20130605”.这样的话日志文件名不会重叠,所以也就不需要日志文件的改名,只需要保存指定的日志个数,删除多余的日志文件即可.
- 如果配置文件中没有“dateext”参数,那么日志文件就需要进行改名了.当第一次进行日志轮替时,当前的“secure”日志,用来保存新的日志.当第二次进行日志轮替时,”secure.1”会自动改名为“secure.2”,当前的“secure”日志会自动改名为“secure.1”,然后也会新建“secure”日志,用来保存新的日志,此以类推.

### 14.3.2 logrotate配置文件

| 参数                    | 参数说明                                                     |
| ----------------------- | ------------------------------------------------------------ |
| daily                   | 日志的轮替周期是每天                                         |
| weekly                  | 日志的轮替周期是每周                                         |
| monthly                 | 日志的轮替周期是每月                                         |
| rotate 数字             | 保留的日志文件的个数 . 0指没有备份                           |
| compress                | 日志轮替时,旧的日志进行压缩                                  |
| create mode owner group | 建立新日志,同时指定新日志的权限与所有者和所属组.如create 0600 root utmp |
|mail address|当日志轮替时,输出内容通过邮件发送到指定的邮件地址.如mail shenc@lamp.net|
|misssingok|如果日志不存在,则忽略该日志的警告信息|
|notifempty| 如果日志为空文件,则不进行日志轮替                            |
|minsize   大小| 日志轮替的最小值,也就是日志一定要达到这个最小值才会轮替,否则就算时间达到也不轮替 |
|size  大小|日志只有大于指定大小才进行日志轮替,而不是按照时间轮替.如size 100k|
|dateext|使用日期作为日志轮替文件的后缀,如secure-20130605|

### 14.3.3 把apache日志加入轮替

```shell
[root@localhost ~]# vim /etc/logrotate.conf
/usr/local/apache2/logs/access_log{
	daily
	create
	rotate 30
}
```

### 14.3.4 logratate命令

```shell
[root@localhost ~]# logrotate [选项] 配置文件名
选项:
	如果此命令没有选项,则会按照配置文件中的条件进行日志轮替
	-v:显示日志轮替过程.加了-v选项,会显示日志的轮替的过程
	-f:强制进行日志轮替.不管日志轮替的条件是否已经符合,强制配置文件中所有的日志进行轮替
```

# 15. 启动流程

##  15.1 CentOS 6.x启动管理

### 15.1.1 系统运行级别

#### 15.1.1.1 运行级别

| 运行级别 | 含义 |
| -------- | ---- |
| 0        | 关机 |
| 1        | 单用户模式,可以想象为windows的安全模式,主要用于系统修复 |
| 2        | 不完全的命令行模式,不含NFS服务 |
| 3        | 完全的命令行模式,就是标准字符界面 |
| 4        | 系统保留 |
| 5        | 图形模式 |
|6|重启动|

#### 15.1.1.2 运行级别命令

```shell
[root@localhost ~]# runlevel 
```

#查看运行级别命令

```shell
[root@localhost ~]# init 运行级别
```

#改变运行级别命令

#### 15.1.1.3 系统默认运行级别

```shell
[root@localhost ~]# vim /etc/inittab
```

id:3:initdefault:

#系统开机后直接进入哪个运行级别

### 15.1.2 系统启动过程

> 启动流程图

![image-20201009135711451](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201009135711451.png)

initramfs 内存文件系统

- CentOS 6.x 中使用initramfs内存文件系统取代了CentOS5.x中的initrd RAM Disk . 他们的作用类似,可以通过启动引导程序加载到内存中,然后加载启动过程中所需要的内核模块,比如USB、SATA、SCSI硬盘的驱动和LVM、RAID文件系统的驱动 

![image-20201010121733248](C:%5CUsers%5CAlienware%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20201010121733248.png)

调用/etc/init/rsS.conf配置文件

- 主要功能是两个: 

  - 先调用/etc/rc.d/rc.sysinit,然后由/etc/rc.d/rc.sysinit配置文件进行Linux系统初始化.
  - 然后再调用/etc/inittab,然后由/etc/inittab配置文件确定系统的默认运行级别.

  由/etc/rc.d/rc.sysinit初始化

  1. 获得网络环境
  2. 挂载设备
  3. 开机启动画面Plymouth( 取替了过往的RHGB )
  4. 判断是否启用SELinux
  5. 显示于开机过程中的欢迎画面
  6. 初始化硬件
  7. 用户自定义模块的加载
  8. 配置内核的参数
  9. 设置主机名
  10. 同步存储器
  11. 设备映射器及相关的初始化
  12. 初始化软件磁盘阵列(RAID)
  13. 初始化LVM的文件系统功能
  14. 检验磁盘文件系统(fsck)
  15. 设置磁盘配额(quota)
  16. 重新以可读写模式挂载系统磁盘
  17. 更新quota(非必要)
  18. 启动系统虚拟随机数生成器
  19. 配置机器(非必要)
  20. 清除开机过程当中的临时文件
  21. 创建ICE目录
  22. 启动交换分区(swap)
  23. 将开机信息写入/var/log/dmesg文件中

  调用/etc/rc.d/rc文件

- 运行级别参数传入/etc/rc.d/rc这个脚本之后,由这个脚本文件按照不同的运行级别启动/etc/rc[0-6].d目录中的相应的程序
  - /etc/rc3.d/k??开头的文件 (？？是数字) , 会按照数字顺序依次关闭
  - /etc/rc3.d/S??开头的文件(？？是数字) , 会按照数字顺序依次启动

  

## 15.2 启动引导程序grub

### 15.2.1 Grub配置文件

![image-20201010142707092](C:%5CUsers%5CAlienware%5CAppData%5CRoaming%5CTypora%5Ctypora-user-images%5Cimage-20201010142707092.png)

![image-20201010143400032](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201010143400032.png)

![image-20201010143643632](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201010143643632.png)

### 15.2.2 Grub加密与字符界面分辨率调整

#### 15.2.2.1 grub加密

[root@localhost ~]# grub-md5-crypt

#生成加密密码串

![image-20201010155001267](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201010155001267.png)

#### 15.2.2.2 纯字符界面分辨率调整

grep “CONFIG_FRAMEBUFFER_CONSOLE” /boot/config-2.6.32.-279.e16.i686

#查询内核是否支持分辨率修改

![image-20201010155430210](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201010155430210.png)

[root@localhost ~]# vim /boot/grub/grub.conf 

```shell
default=0
timeout=5
splashimage=(hd0,0)/grub/splash.xpm.gz
hiddenmenu
title CentOS (2.6.32-279.el6.x86_64)
    root (hd0,0)
    kernel /vmlinuz-2.6.32-279.el6.x86_64 ro root=UUID=0c28f491-5fa6-4911-9e93-8bc07f17600e rd_NO_LUKS  KEYBOARDTYPE=pc KEYTABLE=us rd_NO_MD crashkernel=auto LANG=zh_CN.UTF-8 rd_NO_LVM rd_NO_DM rhgb quiet vga=791
    initrd /initramfs-2.6.32-279.el6.x86_64.img

```









## 15.3 系统修复模式



# 16. 备份与恢复

## 16.1 备份概述

### 16.1.1 Linux 系统需要备份的数据

- /root/目录:
- /home/目录:
- /var/spool/mail/目录:
- /etc/目录:
- 其他目录:

> 安装服务的数据

- apache需要备份的数据
  - 配置文件
  - 网页主目录
  - 日志文件
- mysql需要备份的数据
  - 源码包安装的mysql:/usr/local/mysql/data/
  - RPM包安装的mysql:/var/lib/mysql/

### 16.1.2 备份策略

- 完全备份:完全备份就是指把所有需要备份的数据全部备份,当然完全备份可以备份整块硬盘,整个分区或某个具体的目录 

> 增量备份

![image-20201010145557936](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201010145557936.png)

> 差异备份

![image-20201010145931822](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201010145931822.png)



## 16.2 dump和restore命令

### 16.2.1 dump命令

[root@localhost ~]# dump [选项] 备份之后的文件名 原文件或目录

选项:

​			-level:			就是我们说的0-9十个备份级别

​			-f 文件名:    指定备份之后的文件名

​			-u:					备份成功之后,把备份时间记录在/etc/dumpdtates文件

​			-v:					显示备份过程中更多的输出信息

​			-j:					调用bzlib库压缩备份文件,其实就是备份文件压缩到为.bz2格式

​			-W:				显示允许被dump的分区的备份等级及备份时间

> 　备份分区

dump -0uj -f /root/boot.bak.bz2 /boot/

#备份命令.先执行一次完全备份,并压缩和更新备份时间

cat /etc/dumpdates

#查看备份时间文件

cp install.log /boot/

#复制日志文件到boot分区

dump -1 uj -f /root/boot.bak1.bz2 /boot/

#增量备份/boot分区,并压缩

dump -W

#查询分区的备份时间及备份级别的

> 备份文件和目录

dump -0j -f /root/etc.dump.bz2 /etc/

#完全备份/etc/目录,只能使用0级级别进行完全备份,而不再支持增量备份

### 16.2.2 restore命令

[root@localhost ~]# restore [模式选项] [选项]

模式选项:restore 命令常用的模式有以下四种,这四个模式不能混用.

​		-C:		比较备份数据和实际数据的变化

​		-i:		 进入交互模式,手工选择需要恢复的文件 .

​		-t:		 查看模式,用于查看备份文件中拥有哪些数据 .

​		-r:		 还原模式,用于数据还原.

​	选项:     

​		-f:		 指定备份文件的文件名

mv /boot/vmlinuz-2.6.32-279.e16.i686 /boot/vmlinuz-2.6.32-279.e16.i686.bak

#把/boot 目录中内核镜像文件改个名字

restore -C -f /root/boot/bak.bz2

#restore 发现内核镜像文件丢失

> 查看模式

restore -t -f boot.bak.bz2

> 还原模式

#还原boot.bak.bz2分区备份

#先还原完全备份的数据

mkdir boot.test

cd boot.test/

restore -r -f /root/boot.bak.bz2

#解压缩

restore -r -f /root/book.bak1.bz2

#恢复增量备份数据

#还原/etc/目录的备份etc.dump.bz2

restore -r -f etc.dump.bz2

#还原etc.dump.bz2备份


















