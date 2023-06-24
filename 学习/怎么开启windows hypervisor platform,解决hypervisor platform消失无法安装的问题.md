---
layout: post
title: 怎么开启windows hypervisor platform,解决hypervisor platform消失无法安装的问题
categories: [开发工具,Docker]
tags:  Docker
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/20190318161116970.png
---

# 怎么开启windows hypervisor platform,解决hypervisor platform消失无法安装的问题

> 因为docker desktop需要,花了两天才找到解决方案 尴尬....

![在这里插入图片描述](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/20190318161116970.png)

![在这里插入图片描述](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/2019031816132147.png)

很好,没有安装windows hypervisor platform的机会,但是没关系(ps:此处描述有误中文名称应该是虚拟机监控程序平台)
然后cmd 或powershll 管理员身份运行
Dism /online /Get-Features
可以查看到hypervisor platform是禁用状态





另外:

baidu.com 搜索解决方案 总是找不到,尝试在www.google.com搜索,出了一堆解决方案,但解决方案都是英语,但对我来影响不大,就这段.

用了两个方法,重启后 神奇解决了,不知道才是哪个解决,干脆发两个方法 大家可以尝试！



hyperv-enable.bat

```
@echo off
echo "NOTE: you must run this script at administrator level"
bcdedit /set hypervisorlaunchtype auto
echo "press enter to reboot ..."
pause
shutdown /r
```

hyperv-disable.bat

```
@echo off
echo "NOTE: you must run this script at administrator level"
bcdedit /set hypervisorlaunchtype off
echo "press enter to reboot ..."
pause
shutdown /r
```

to switch hyper-V on/off simply right-click on the bat file and select ‘run as administrator’ … after a reboot, the hyper-V service will be updated.

[![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/hyperv-config.png)](http://blog.electrongoo.com/wp-content/uploads/2017/11/hyperv-config.png)

<iframe ng-non-bindable="" frameborder="0" hspace="0" marginheight="0" marginwidth="0" scrolling="no" tabindex="0" vspace="0" width="100%" id="I0_1600885297097" name="I0_1600885297097" src="https://apis.google.com/u/0/se/0/_/+1/fastbutton?usegapi=1&amp;size=tall&amp;hl=en&amp;origin=http%3A%2F%2Fblog.electrongoo.com&amp;url=http%3A%2F%2Fblog.electrongoo.com%2Findex.php%2Fenable-and-disable-hyper-v-service-on-windows%2F&amp;gsrc=3p&amp;ic=1&amp;jsh=m%3B%2F_%2Fscs%2Fapps-static%2F_%2Fjs%2Fk%3Doz.gapi.zh_CN.NpVFPhFgCzw.O%2Fam%3DwQE%2Fd%3D1%2Fct%3Dzgms%2Frs%3DAGLTcCPZqasShkDqgnl-YBuYCH80bk1FKw%2Fm%3D__features__#_methods=onPlusOne%2C_ready%2C_close%2C_open%2C_resizeMe%2C_renderstart%2Concircled%2Cdrefresh%2Cerefresh%2Conload&amp;id=I0_1600885297097&amp;_gfid=I0_1600885297097&amp;parent=http%3A%2F%2Fblog.electrongoo.com&amp;pfname=&amp;rpctoken=32279021" data-gapiattached="true" style="border: 0px none; font-family: inherit; font-size: 16px; font-style: inherit; font-weight: inherit; margin: 0px; outline: 0px; padding: 0px; vertical-align: baseline; max-width: 100%; min-height: 25px; position: absolute; top: -10000px; width: 450px;"></iframe>

SHARE