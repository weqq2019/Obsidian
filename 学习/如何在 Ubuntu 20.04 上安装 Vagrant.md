---
layout: post
title:  如何在 Ubuntu 20.04 上安装 Vagrant
categories: [开发工具,Vagrant]
tags: Vagrant
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920225214616.png
---

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920225214616.png)

[Vagrant](https://www.vagrantup.com/)是一个命令行工具，用于构建和管理虚拟开发环境。

默认情况下，Vagrant 在 VirtualBox, Hyper-V, 和 Docker 之上准备环境。支持其他提供者，例如， Libvirt (KVM), VMware and AWS 可以通过 Vagrant 插件系统启用。

Vagrant 通常被开发者用来建立匹配生产环境的开发环境。

这篇文章描述如何在 Ubuntu 20.04 机器上安装 Vagrant。我们将会使用 VirtualBox，Vagrant 默认的提供者。

## 一、在 Ubuntu 上安装 Vagrant

我们将会在 VirtualBox 的基础上提供虚拟机。

如果 [VirtualBox](https://linuxize.com/post/how-to-install-virtualbox-on-ubuntu-20-04/) 没有安装在你系统上，你可以运行下面的命令安装它：

```bash
sudo apt update
sudo apt install virtualbox
```

Vagrant 软件包，在 Ubuntu 源仓库中提供，并且不经常更新。我们将会从官方 Vagrant 网站下载并安装最新版的 Vagrant。

在写这篇文章的时候，Vagrant 最新版是 2.2.9。浏览 [Vagrant 下载页面](https://www.vagrantup.com/downloads.html)，看看有没有 Vagrant 最新版本可用。

使用 wget 下载 Vagrant 软件包：

```bash
curl -O https://releases.hashicorp.com/vagrant/2.2.9/vagrant_2.2.9_x86_64.deb
```

一旦下载完成，输入下面的命令安装它：

```bash
sudo apt install ./vagrant_2.2.9_x86_64.deb
```

想要验证安装是否成功，运行下面的命令，打印 Vagrant 版本：

```bash
vagrant --version
```

输出类似下面这样：

```bash
Vagrant 2.2.9
```

## 二、Vagrant 入门

创建 Vagrant 项目非常简单，在项目根目录下定义个 Vagrantfile。

运行下面的命令，创建文件夹，并且 cd 切换到这个目录：

```bash
mkdir ~/my-vagrant-project
cd ~/my-vagrant-project
```

下一步，使用`vagrant init`加上你想使用的盒子，初始化一个新的 Vagrantfile。

盒子就是Vagrant 环境的软件包格式。你可以在 [Vagrant box 页面](https://app.vagrantup.com/boxes/search) 找到盒子列表。

在这个例子中，我们使用`centos/8`盒子：

```bash
vagrant init centos/8
```

输出：

```bash
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
```

Vagrantfile 是一个 Ruby 文件，它用来描述如何配置和提供虚拟机。你可以打开 [Vagrantfile](https://www.vagrantup.com/docs/vagrantfile/)，阅读注释，并且根据你自己的需求，做出相应的调整。

运行`vagrant up`命令按照 Vagrantfile 指定的内容来创建并且配置虚拟机。

```bash
vagrant up
==> default: Configuring and enabling network interfaces...
    default: SSH address: 192.168.121.74:22
    default: SSH username: vagrant
    default: SSH auth method: private key
==> default: Rsyncing folder: /home/linuxize/Vagrant/my-vagrant-project/ => /vagrant
```

Vagrant 将项目目录挂载到虚拟机的 `/vagrant`目录。这允许你在你的主机上操作你的项目文件。

想要使用 SSH 进入你的虚拟机，运行：

```bash
vagrant ssh
```

你可以使用下面的命令停止虚拟机：

```bash
vagrant halt
```

想要释放所有创建虚拟机过程中的资源，输入：

```bash
vagrant destroy
```

## 三、总结

我们向你展示了如何在 Ubuntu 20.04 上安装 Vagrant 以及创建一个基本的 Vagrant 项目。

想要查找更多关于 Vagrant 的信息，浏览 [Vagrant 官方文档页面](https://www.vagrantup.com/docs/index.html)。