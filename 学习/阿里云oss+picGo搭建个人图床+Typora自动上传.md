---
layout: post
title:  阿里云oss+picGo搭建个人图床+Typora自动上传
categories: [WEB开发,域名与网站]
tags:  域名与网站
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164507229.png
---

## 阿里云OSS

### 阿里云创建Bucket

- 阿里云控制台 -> 对象存储OSS -> 创建Bucket，权限要改为公共读。

![image-20200920164200365](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164200365.png)

- 如果有自己的域名，可以通过传输管理 -> 域名管理，来绑定自己的域名。

![image-20200920164246057](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164246057.png)

### 创建子用户AccessKey

- 进入用户的AccessKey管理

![image-20200920164312343](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164312343.png)

- 创建 RAM 子用户 AccessKey 来进行 API 调用。这样操作的目的是为了降低账号的风险。

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164336172.png)

- 创建用户时，注意勾选 **编程访问**

![image-20200819221300879](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164355095.png)

- 创建成功后，弹出下图信息，这里的AccessKey Secret只显示一次，自己备份下来

![image-20200819221611743](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164428722.png)

- 给刚创建的用户添加管理OSS权限

![image-20200819221758958](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164446139.png)

以上，阿里云OSS准备工作完成。

## picGo图床

### 配置阿里OSS

打开picGo，在图床设置中填写需要的配置参数。

![image-20200819222437536](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164507229.png)

- KeyId和KeySecret分别是上一步新创建用户的AccessKey ID和AccessKey Secret。
- 存储空间名为上一步创建的Bucket名称。
- 存储区域为

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164536295.png)

- 存储路径是存储图片的位置，要求以/结尾。
- 自定义域名可以不填写，或者填写上一步绑定的域名。

### 测试上传

完成上一步配置后。截完图，可以点击剪贴板图片上传，也可以使用快捷键快速上传剪贴板图片（快捷键在PICGO设置中可以设置）

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164603220.png)

## Typora自动上传

使用Typora编写markdown时，通过设置Typora的图像上传设置，我们可以在截图粘贴到Typora中，实现自动上床阿里云OSS，并更改截图的url。

![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920164619980.png)