---
layout: post
title:  "Git Base 中文显示乱码问题"
categories: [开发工具,git]
tags:  git
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200918023234150.png
---

---


今天做一个实验的时候要用到Git base工具 ping 但是输出有中文,导致显示乱码,如下

<img src="https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200918023234150.png" alt="image-20200918023234150" />

百度找了一下，
直接右键，选择Options…——>Text——>Locale里面选择zh_CN,Character set选择UTF-8，但是关闭再打开运行还是乱码，遂检查Java文件的编码方式，发现是utf-8没错，然后再去百度找，试着把character set改成GBK，成功。

![在这里插入图片描述](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/4b60f60000137db5722078656963d363.png)

成功显示不乱码：

![image-20200918023429653](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200918023429653.png)