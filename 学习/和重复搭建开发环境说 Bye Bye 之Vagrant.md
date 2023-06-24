---
layout: post
title:  "和重复搭建开发环境说 Bye Bye 之Vagrant"
categories: [开发工具,Vagrant]
tags:  Vagrant
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-516f509bd41ff64e78ff6a090b68c3e6_720w.jpg
---

“ 入职就赶紧投入开发，别费时间搭开发环境。——编程三分钟**”**

每每**新**同事入职，都要在自己电脑上配置**一堆**环境，**费**神费力；每每开发测试都要**重新**配置开发环境，手工搭建，步骤很**繁琐**，极易**出错**。

**大神**在时，**大神**搭建，大神**不在**，以手抚膺**坐长叹**。**为此，**VVVV**Vagrant**横空出世！！！

虚拟机编排工具Vagrant



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-516f509bd41ff64e78ff6a090b68c3e6_720w.jpg)



他，基于**虚拟机**，能打造出**完美**的物理隔离！

他，**一次**搭建，**处处**使用，拷贝一个镜像就能让新员工**立即投入开发**，当属**老板**的**最爱**！

他，只需要**一个文本**，寥寥**几行**，就能**驾驭**网络配置、建立**集群**！

良好的**第三方**支持也让他如鱼得水，支持**shell**脚本、支持**ansible**自动部署等等。他就是我们的主角 **Vagrant** 。

这次，我们就以**搭建python开发环境**为例，享受vagrant给我们带来的便利。

### **安装**

mac环境两行命令

```text
brew cask install virtualbox
brew cask install vagrant
```

其他环境下载两个安装包即可
vagrant包 [https://www.vagrantup.com/downloads.html](https://link.zhihu.com/?target=https%3A//www.vagrantup.com/downloads.html)
virtualbox [https://www.virtualbox.org/wiki/Downloads](https://link.zhihu.com/?target=https%3A//www.virtualbox.org/wiki/Downloads)

检查是否安装成功

```text
$ vagrant version
Installed Version: 2.2.5
Latest Version: 2.2.5

You're running an up-to-date version of Vagrant!
```

### **初始化环境**

第一种下载镜像的方法

```text
vagrant box add --provider virtualbox centos/7
```

其中`--provider virtualbox`代表校验是否是virtualbox官方提供
第二种下载方法

```text
vagrant box add  --name centos/7  --provider virtualbox  /Users/pzqu/Documents/code/test/vbox/centos_virtualbox.box
```

此处的`/Users/pzqu/Documents/code/test/vbox`是我的选定的下载目录

对box的一系列操作命令文档见这里[https://www.vagrantup.com/docs/cli/box.html](https://link.zhihu.com/?target=https%3A//www.vagrantup.com/docs/cli/box.html)。

初始化

```text
cd /Users/pzqu/Documents/code/test/vbox
vagrant init centos/7
```

此时目录下会生成一个`Vagrantfile`文件，此文件就是自动化配置的关键

[https://www.vagrantup.com/docs/vagrantfile/](https://link.zhihu.com/?target=https%3A//www.vagrantup.com/docs/vagrantfile/)

看一看里面的注释大概就知道怎么写了，主要是ruby的语法，可以挂载本地目录到虚拟机里，配置网络（接入公网、仅虚拟机访问都可以）等。

除了对虚拟机进行一些配置外，还可以通过各类Provisioner自动化地安装软件、调整配置。
详见 [https://www.vagrantup.com/docs/provisioning/](https://link.zhihu.com/?target=https%3A//www.vagrantup.com/docs/provisioning/)

我的配置比较简单，使用centos/7的系统，把本机代码项目的目录挂载到`/data/code`目录就可以了。

启动虚拟机以后直接在虚拟机里安装开发环境，最后再打成镜像就妥了。

配置如下

```text
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.synced_folder "/Users/pzqu/Documents/code/gerrit", "/data/code"
end
```

挂载文件目录的时候报错



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-de258ff35d8c02ed5be9db1c6b10a6a2_720w.jpg)



安装此插件即可

```text
vagrant plugin install vagrant-vbguest
```

### **搭建开发环境**

在`Vagrantfile`所在目录下，使用`vagrant up`启动虚拟机
再用`vagrant ssh`登陆虚拟机

然后执行以下命令自动安装我们想要的python环境，注意`requirements.txt`是`python`项目自动生成的

```text
pip install -r requirements.txt
```

补充：自动生成`requirements`文件的方法

```text
pip freeze > requirements.txt
```

### **配置pycharm**

打开配置，添加插件



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-de258ff35d8c02ed5be9db1c6b10a6a2_720w.jpg)



配置`Vagrant`环境



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-c71324d75c136ef8a40af8a8fade4376_720w.jpg)



指定虚拟机中的Python路径，第一步选 show all



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-1806e56917afadcb6c6552bbf96df9d1_720w.jpg)



选择`Vagrant`选择镜像目录与虚拟机中`python`路径



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-f94f5e61b79230616e76758e58f04b93_720w.jpg)





![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-b478d084fce396224cc96c82cba7364d_720w.jpg)



配置启动方式，这里我生成swagger，主要是`Python interpreter`python路径，`Working direftory`项目路径（注意是虚拟机中映射的路径，我这里在上一节配置的`/data/code`,我们在本地开发的时候会自动同步修改）



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-397d6ff5b5da5897b4e99a6a05828581_720w.jpg)



运行



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-dd6eda4adf30a3d339a83088d55023de_720w.jpg)



### **导出box镜像文件给别人使用**

1.运行 vboxmanage list vms 命令，可以看出我们的vagrant下的虚拟机列表(我的虚拟机只有一个box，“vbox_default_1563884434349_3918“。)

```text
$ vboxmanage list vms
"vbox_default_1563884434349_3918" {59864f0b-9731-4839-baa2-95d9a6aab731}
```

1. 导出box镜像
   先关机，再导出。vagrant package是导出box的打包命令

```text
vagrant package --base vbox_default_1563884434349_3918 --output centos7_hanah_environment.box
```

`--base` 代表本地 
`vbox_default_1563884434349_3918`是你要导出的box的名称 
`--output`代表导出 
`centos7_hanah_environment.box` 表示导出后的box名为`centos7_hanah_environment.box`，并保存在当前目录下

1. 接下来你会看到如下内容，就是导出成功了

```text
$ vagrant package --base vbox_default_1563884434349_3918 --output centos7_hanah_environment.box
==> vbox_default_1563884434349_3918: Exporting VM...
==> vbox_default_1563884434349_3918: Compressing package to: /Users/pzqu/Documents/code/test/vbox/centos7_hanah_environment.box
```

喝完一瓶奶的功夫就完成了，这取决于你的box的大小，我的box大约900M。
这下直接发给你的朋友，一句命令就获得了一个和你完全相同的开发/测试环境。

```text
$ vagrant box add centos7_hanah_environment ./centos7_hanah_environment.box
==> box: Box file was not detected as metadata. Adding it directly...
==> box: Adding box 'centos7_hanah_environment' (v0) for provider:
    box: Unpacking necessary files from: file:///Users/pzqu/Documents/code/test/vbox/centos7_hanah_environment.box
==> box: Successfully added box 'centos7_hanah_environment' (v0) for 'virtualbox'!
```


vagrant box add 别名 box名

### **其他想法**

听起来vagrant所做的这些事情和docker有很多重叠的地方，为什么不直接用docker来做呢？不仅可以一秒启动一个最适合的环境，而且又轻量又纯净。

权衡利弊，vagrant本身并不是虚拟化技术，要把他跑起来还要安装virtualbox等虚拟化平台，他更像是虚拟机的外挂程序、编排工具；针对的是批量虚拟机的管理，常常用于瞬间创建一个开发环境。

而docker本身就是虚拟化技术，构建迅速，不占用资源；针对的是应用程序的编排，常常用于统一开发环境与生产环境。

说来说去，与其说是vagrant与docker，不如说使用是虚拟化平台与容器之间的区别。



![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/v2-dd6eda4adf30a3d339a83088d55023de_720w.jpg)



docker还是依赖于系统内核，如果内核不同，需要重新构建。

有时间我们来聊聊docker创建开发环境，有机会再来聊聊`Docker Machine`



vagrant是一个工具，用于创建和部署虚拟化开发环境的。

拿VirtualBox举例，VirtualBox会开放一个创建虚拟机的接口，Vagrant会利用这个接口创建虚拟机，并且通过Vagrant来管理，配置和自动安装虚拟机。

# 常见命令

| 命令               | 解释                  |
| ------------------ | --------------------- |
| vagrant box list   | 查看目前已有的box     |
| vagrant box add    | 新增加一个box         |
| vagrant box remove | 删除指定box           |
| vagrant init       | 初始化配置vagrantfile |
| vagrant up         | 启动虚拟机            |
| vagrant ssh        | ssh登录虚拟机         |
| vagrant suspend    | 挂起虚拟机            |
| vagrant reload     | 重启虚拟机            |
| vagrant halt       | 关闭虚拟机            |
| vagrant status     | 查看虚拟机状态        |
| vagrant destroy    | 删除虚拟机            |
