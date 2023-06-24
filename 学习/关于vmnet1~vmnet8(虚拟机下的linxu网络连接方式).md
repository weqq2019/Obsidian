---
layout: post
title: 关于vmnet1~vmnet8(虚拟机下的linxu网络连接方式)
categories: [开发工具,VMware]
tags: VMware
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929061116353.png
---

# 关于vmnet1~vmnet8(虚拟机下的linxu网络连接方式)

先说vmnet0，实际上就是一个虚拟的网桥，这个网桥有很若干个端口，一个端口用于连接你的Host，一个端口用于连接你的虚拟机，他们的位置是对等的，谁也不是谁的网关。所以在Bridged模式下，你可以让虚拟机成为一台和你的Host相同地位的机器，如图：  ![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929060748387.png)   再说vmnet1，这是一个Host-Only网络模式，这是用于建立一个与世隔绝的网络环境所用到的，其中vmnet1也是一个虚拟的交换机，交换机的一个端口连接到你的Host上，另外一个端口连接到虚拟的DHCP服务器上（实际上是vmware的一个组件），另外剩下的端口就是连虚拟机了。虚拟网卡“VMWare Virtual Ethernet Adapter for VMnet1”作为虚拟机的网关接口，为虚拟机提供服务。在虚拟机启动之后，如果你用ipconfig命令，你会很清楚的看到，你的默认网关就是指向“VMWare Virtual Ethernet Adapter for VMnet1”网卡的地址的。（实际上它并不能提供路由，这是VMware设计使然，它是干了除了提供路由之外的一些事情——实际上是我也不知道它干了什么事情），这里没有提供路由主要表现在没有提供NAT服务，使得虚拟机不可以访问Host-Only模式所指定的网段之外的地址，看图可以很明白：  ![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929060806395.png)   再说vmnet8，这是一个NAT方式，最简单的组网方式了，从主机的“VMWare Virtual Ethernet Adapter for VMnet8”虚拟网卡出来，连接到vmnet8虚拟交换机，虚拟交换机的另外的口连接到虚拟的NAT服务器（这也是一个Vmware组件），还有一个口连接到虚拟DHCP服务器，其他的口连虚拟机，虚拟机的网关即是“VMWare Virtual Ethernet Adapter for VMnet8”网卡所在的机器，废话，这肯定就是你的Host机器啦。同样，用ipconfig也可以看出来，你的虚拟机的默认网关也指向了你的“VMWare Virtual Ethernet Adapter for VMnet8”虚拟网卡地址。相比之下，可以看出来，NAT组网方式和Host-Only方式，区别就在于是否多了一个NAT服务，看图：  ![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929060826824.png)  一些初学者对VMware虚拟机中的桥接、VMnet1(仅host方式)、VMnet8(NAT方式)，我把VMware各网卡的意义做了三张图，希望对大家有所帮助。  显示不全，请大家另存观看。      ![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929061116353.png) 

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929061050786.png)



![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200929060931038.png)