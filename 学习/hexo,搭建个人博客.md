---
layout: post
title:  hexo,搭建个人博客
categories: [WEB开发,域名与网站]
tags:  hexo
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003213944729.png
---

![image-20201003213944729](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003213944729.png)

### 本文概要

- hexo 使用，及怎么去改主题的模板
- 阿里云服务器，搭建 nginx ,配置 nginx 缓存
- 百度、谷歌 seo 优化，让你的网站可以被搜索到
- 阿里 oss 作为图片服务器
- CDN 加速提高首屏渲染
- shell 脚本一键部署到 nginx 目录下，将所需静态资源上传到 oss

## Hexo 介绍

hexo 会解析 `markdown` 语法 生成对应的 html ，主题就是 css 样式。

我自己的 hexo [GitHub](https://github.com/zhangpanqin/my-hexo-theme-matery) 克隆之后 `yarn install` 安装依赖。`hexo s` 本地预览效果。

[yarn 中文教程](https://yarn.bootcss.com/)

如果是用 `npm` 安装的依赖包的话，请将 `yarn.lock` 先删除，再 `npm install` 安装。我已在项目下 `.npmrc` 配置依赖包从淘宝镜像下载。

`root` 为项目根路径。





bash

```bash
# 本地预览
hexo s

# 根据配置文件和主题，将 root/source/_post 下的 markdown 文件生成 html 内容
hexo g

# 清空 hexo g 生成的内容，内容在 root/public 
hexo clean

# 将本地生成 url 链接推送到百度，让百度爬取其中的内容进行索引
hexo d

# 根据 标题名称  在root/source/_post 生成 markdown 文件
hexo new post 标题名称
```

### 配置友链

`root/source/_post/friends.json` 配置友链。



![image-20200306225510922](http://oss.mflyyou.cn/blog/20200306225510.png?author=zhangpanqin)

**image-20200306225510922**



### 配置音乐

`root/source/_post/musics.json` 配置音乐列表。



![image-20200306225547485](http://oss.mflyyou.cn/blog/20200306225547.png?author=zhangpanqin)

**image-20200306225547485**



### 导航-关于

`root/source/about/index.md` 配置个人信息。



![image-20200307121049901](http://oss.mflyyou.cn/blog/20200307121050.png?author=zhangpanqin)

**image-20200307121049901**



### 导航-留言

`root/source/contact/index.md` 配置留言展示信息。



![image-20200307121113555](http://oss.mflyyou.cn/blog/20200307121113.png?author=zhangpanqin)

**image-20200307121113555**



### 导航-标签/分类/归档

以上配置信息是在文档的 markdown 文件中配置，然后会根据这些信息生成以上导航的内容。





txt

```txt
---
# 名称
title: {{ title }}
# 文章日期
date: {{ date }}
# 是否在页面推荐文章列表展示
top: false
# 是否在首页轮播
cover: false
# 查看文章的密码, sha256 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
password: 
# 文章目录
toc: true
# 统计文章
mathjax: true
# 文章摘要
summary:
# 文章标签
tags:
# 文章分类
categories:
# 文档关联图片,可以配置 url,没配置的话,自动从主题配置文件的 featureImages 属性中自动选取一个
img:
---
```

文档 md 文件最前面的这些内容就会被利用生成 `标签` `分类` `归档` 内容。

`root/_config.yml` 为 hexo 的配置文件。

`root/themes/_config.yml` 为主题配置文件。

我在配置文件中加看注释，基本看注释就能明白。我重点说几个重要的功能。

### gitalk 配置

基本和这个 [gitalk readme](https://github.com/gitalk/gitalk/blob/master/readme-cn.md)



![image-20200306222243375](http://oss.mflyyou.cn/blog/20200306222243.png?author=zhangpanqin)

**image-20200306222243375**



创建一个公共仓库作为你的博客留言，这个是基于 github 仓库下的 issue 提供的功能。

点击你申请的 app,查看 gitalk 的配置信息



![image-20200306222528779](http://oss.mflyyou.cn/blog/20200306222528.png?author=zhangpanqin)

**image-20200306222528779**



注意 gitalk 的 配置信息不要泄露





yaml

```yaml
# Gitalk 评论模块的配置，默认为不激活
gitalk:
  enable: true
  # 配置你的用户名
  owner: zhangpanqin
  # 配置一个公共仓库储存聊天记录。
  repo: hexo-gitalk
  oauth:
      # 填写你申请的 Client ID
    clientId: 
    # 填写 Client Secret
    clientSecret: 
  # 配置你的用户名
  admin: zhangpanqin
```



![image-20200306222904462](http://oss.mflyyou.cn/blog/20200306222904.png?author=zhangpanqin)

**image-20200306222904462**



### valine

gitalk 是需要登录 `github` 才能登录的，valine 是不需要登录就可以留言的。

[官网申请账号](https://www.leancloud.cn/)



![image-20200306223337173](http://oss.mflyyou.cn/blog/20200306223337.png?author=zhangpanqin)

**image-20200306223337173**



申请好账号，先创建自己的应用，然后将 `ApplD` 和 `AppKey` 配置到主题文件中去。注意 valine 的 配置信息不要泄露





yaml

```yaml
valine:
  enable: true
  appId: 
  appKey: 
  notify: false
  verify: false
  visitor: true
  avatar: 'mm' # Gravatar style : mm/identicon/monsterid/wavatar/retro/hide
  pageSize: 10
  placeholder: 'just go go' # Comment Box placeholder
  background: /medias/comment_bg.png
```

> valine 评论如下



![image-20200306223749651](http://oss.mflyyou.cn/blog/20200306223749.png?author=zhangpanqin)

**image-20200306223749651**



### 不蒜子统计

可以在页脚展示你的网站访问量和访问人次，但是会拖慢页面加载，我将其关闭了。





yaml

```yaml
# 不蒜子(http://busuanzi.ibruce.info/) 网站统计,为了网站加载速度,展示关闭
busuanziStatistics:
  enable: false
  totalTraffic: true # 总访问量
  totalNumberOfvisitors: true # 总人次
```

### 页面资源配置前置路径

以前的版本，资源只能加载当前网站下的资源，现在可以配置路径前缀。将静态的 css,js 库 、图片资源放到阿里 oss 上去，再利用 cdn 加速，可以提高首屏渲染速度。本地调试的时候 配置 `url` 为空





yaml

```yaml
# 静态资源前缀路径
jsDelivr:
    url:  
```

### 扩展修改

`root/themes/matery/layout` 为模板文件，你会 html 和 css 就能修改，模板的语法也很简单，当你看几篇模板基本就学会了。

### 静态资源位置

`root/themes/matery/source` 为静态资源位置，可将这些资源放到 oss 上去，通过 cdn 加速。

## 部署

基于以上步骤你就可以 `hexo s` 本地预览，我们要部署到服务器上去。

阿里云上买个服务器，我装的是 cenos 7.7系统。

### 创建新用户

为了安全不要用 root 用户操作你的远程服务器。

在阿里云控制台创建新的用户，以后用这个用户操作远程服务器。





bash

```bash
# 创建 hexo 用户
adduser hexo

# 修改 hexo 的密码
passwd admin12345

# 给 hexo 赋予 sudo 命令权限

# 在 root 下运行，修改文件的可写性
chmod  700 /etc/sudoers

# /etc/sudoers 文件中填写 rabbitmq ALL=(ALL)      PASSWD:ALL
# 在文件中下拉，找到  root    ALL=(ALL)       ALL
# 在找到的上述内容下添加，便于维护
admin ALL=(ALL)      PASSWD:ALL

# 权限给了之后，修改文件 /etc/sudoers 为只读性
chmod  400 /etc/sudoers
```

### 配置 ssh

配置 ssh 之后，你以后只需要。





bash

```bash
# mflyyou.cn 为你的服务器
ssh mflyyou.cn
```





bash

```bash
# 生成秘钥
ssh-keygen -o -t rsa  -b 4096 -c "生成秘钥对的说明"

# 指定秘钥生成时路径 /Users/zhangpanqin/.ssh/mflyyou_server_rs.pub

# 将公钥 copy 到 server 中 hexo 为以后登录的用户 ip 为你远程服务器 ip
ssh-copy-id -i /Users/zhangpanqin/.ssh/mflyyou_server_rs.pub hexo@id

# 注意那个用户
# 或者登录 server 将公钥内容拷贝到了 ~/.ssh/authorized_keys


# 验证登录 这个是公钥对应的私钥
ssh -T /Users/zhangpanqin/.ssh/mflyyou_server_rs hexo@ip
```

#### 配置登录信息

```
~/.ssh/config
```



![image-20200306233517287](http://oss.mflyyou.cn/blog/20200306233517.png?author=zhangpanqin)

**image-20200306233517287**



Host 之后配置的是别名， ssh mflyyou 就会找 HostName 对应的 ip 登录。

User 配置对应的 用户

IdentityFile 配置对应的私钥文件

以上完成就可以 `ssh mflyyou` 登录了。



![image-20200306233759748](http://oss.mflyyou.cn/blog/20200306233759.png?author=zhangpanqin)

**image-20200306233759748**



### 安装 nginx

[nginx 安装教程](https://nginx.org/en/linux_packages.html#RHEL-CentOS)

默认的网站目录为： /usr/share/nginx/html

默认的配置文件为：/etc/nginx/nginx.conf

自定义配置文件目录为: /etc/nginx/conf.d/





bash

```bash
# 配置开机启动
sudo systemctl enable nginx
sudo systemctl stop nginx
sudo systemctl start nginx
sudo systemctl restart nginx
# 查看 nginx 运行状态
sudo systemctl status nginx

# 检查配置文件 配置是否正确
sudo nginx -t

# 重新加载配置文件
sudo nginx -s reload
```

### 修改配置文件

`/etc/nginx/nginx.conf` 配置缓存





nginx

```nginx
user nginx;
worker_processes auto;
error_log /var/log/nginx/error.log;
pid /run/nginx.pid;
# Load dynamic modules. See /usr/share/doc/nginx/README.dynamic.
include /usr/share/nginx/modules/*.conf;

events {
    worker_connections 1024;
}

http {
    log_format main '$remote_addr - $remote_user [$time_local] "$request" '
    '$status $body_bytes_sent "$http_referer" '
    '"$http_user_agent" "$http_x_forwarded_for"';

    access_log /var/log/nginx/access.log main;

    sendfile on;
    tcp_nopush on;
    tcp_nodelay on;
    keepalive_timeout 65;
    types_hash_max_size 2048;
    proxy_hide_header X-Powered-By;
    proxy_hide_header Server;

    # 开启gzip
    gzip on;

    # 启用gzip压缩的最小文件；小于设置值的文件将不会被压缩
    gzip_min_length 1k;

    # gzip 压缩级别 1-10
    gzip_comp_level 2;

    # 进行压缩的文件类型。

    gzip_types text/plain application/javascript application/x-javascript text/css application/xml text/javascript application/x-httpd-php image/jpeg image/gif image/png;

    # 是否在http header中添加Vary: Accept-Encoding，建议开启
    gzip_vary on;


    include /etc/nginx/mime.types;
    default_type application/octet-stream;
   include /etc/nginx/conf.d/*.conf;


    server {
        listen 80 default_server;
        listen [::]:80 default_server;
        server_name _;
        root /usr/share/nginx/html;
        server_tokens off;
        # Load configuration files for the default server block.
        include /etc/nginx/default.d/*.conf;

        location / {
        }

        location ~* \.(html|xml)$ {
            access_log off;
            add_header Cache-Control no-cache;
        }

        location ~* \.(css|js|png|jpg|jpeg|gif|gz|svg|mp4|mp3|ogg|ogv|webm|htc|woff2|ico|woff|ttf)$ {
            # 同上，通配所有以.css/.js/...结尾的请求
            access_log off;
            # 10 d
            add_header Cache-Control "public,max-age=864000";
        }
        error_page 404 /404.html;
        location = /40x.html {
        }

        error_page 500 502 503 504 /50x.html;
        location = /50x.html {
        }
    }
}
```

主要添加了 `html` 和 `xml` 使用协商缓存，其余静态资源使用强缓存。开启 gzip。

`Cache-Control` 为 http 1.1 关于缓存的配置，优先级最高。

add_header Cache-Control “public,max-age=864000” 配置强缓存。

静态资源几乎不变，全部强缓存。访问的时候，在配置的 max-age 内只要浏览器有缓存直接拿，而不会问服务器。没有缓存的话，访问服务器

add_header Cache-Control no-cache; 配置协商缓存。

html 和 xml 文件是生成的，每次可能会变，配置协商缓存，每次访问先询问服务器有没有变化，没变化走缓存，变化从服务器拿。

部署基于以上部分就可以了。但是美中不足的是 首次加载的时候还是卡。为了解决这个问题，也为了写 markdown 的时候图片上传方便，直接买了一个 oss 和 cdn。oss 和 cdn 一年花费会在 100以内。

如果对 oss 和 cdn 不知道是什么，建议直接部署到阿里云服务器就行

[阿里云服务器推广](https://www.aliyun.com/sale-season/2020/procurement-new-members?userCode=hmiptg58)

## 阿里 oss

我买 oss 的原因是为了用 `typora` 写文章的时候上传图片省事 ，在 `Picgo` 上配置阿里 oss 图床就行。



![image-20200307102712474](http://oss.mflyyou.cn/blog/20200307102712.png?author=zhangpanqin)

**image-20200307102712474**





![image-20200307105001747](http://oss.mflyyou.cn/blog/20200307105001.png?author=zhangpanqin)

**image-20200307105001747**



oss 提供了图形化上传 和 脚本上传。结合 `shell` 可以一键将静态资源上传 oss，html 相关上传 nginx 目录下。



![image-20200307103458966](http://oss.mflyyou.cn/blog/20200307103459.png?author=zhangpanqin)

**image-20200307103458966**



创建之后不要忘了设置防盗链。

然后下图的`传输管理` 选项中开启 cdn 加速，cdn 选择流量计费，20 元 100g。oss 外网访问流量会收费（一年也不会超过一百块），如果你想省钱，可以买和你的阿里云服务器相同区域的，然后让访问走内网。



![image-20200307103817414](http://oss.mflyyou.cn/blog/20200307103817.png?author=zhangpanqin)

**image-20200307103817414**



### CDN



![image-20200307104129580](http://oss.mflyyou.cn/blog/20200307104129.png?author=zhangpanqin)

**image-20200307104129580**



`边缘脚本` 语法看阿里官方指南就可以看懂了，根据自己需求添加。比如给图片加水印，所有请求都会给加上 oss 上的访问参数，使所有的图片都有水印效果。

你也可以通过 `回源配置` 将流量回源到你的阿里云服务器， cdn 回源 oss 也是要收费的。

## SEO

### 提交你的链接，让百度索引

[百度站长工具](https://ziyuan.baidu.com/linksubmit/index)

提交你的链接



![image-20200307113739724](http://oss.mflyyou.cn/blog/20200307113739.png?author=zhangpanqin)

**image-20200307113739724**





![image-20200307113904879](http://oss.mflyyou.cn/blog/20200307113904.png?author=zhangpanqin)

**image-20200307113904879**



在 `roo/_config.yml`将 site 对应 host，token 对应 token。`hexo d` 就会将链接推送百度。我写的脚本，deploy.sh 会自动推送。

自动推送，会在你访问链接的时候，推送百度，只需配置就可以了。





yml

```yml
# 推送你需要让百度索引的链接
baiduPush: true
```

### 百度分析

[百度分析](https://tongji.baidu.com/)

![image-20200307114720921](http://oss.mflyyou.cn/blog/20200307114721.png?author=zhangpanqin)

**image-20200307114720921**

填写上述 id





yaml

```yaml
baiduAnalytics:
    enable: true
    # 百度分析 id
    id: 
```

### google 分析

[google 分析](https://analytics.google.com/analytics/web/)



![image-20200307115610409](http://oss.mflyyou.cn/blog/20200307115610.png?author=zhangpanqin)

**image-20200307115610409**



将跟踪 id 配置到 主题配置文件中





yaml

```yaml
googleAnalytics:
  enable: true
  # 谷歌分析配置申请之后填写你的 id
  id: 
```

[google search console](https://search.google.com/search-console)

在 search console 中添加的你的网站网址，这样 google 会爬取你的网站内容索引。

![image-20200307115742082](http://oss.mflyyou.cn/blog/20200307115742.png?author=zhangpanqin)

**image-20200307115742082**

提交你的站点地图，让 google 知道爬取哪些页面。

以上配置完成后，过几天就会看到以下效果。百度的更慢，我都 10天了还没动静。



![](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201003213711972.png)

**image-20200307115902993**



## 脚本一键部署网站





shell

```shell
BASE_DIR=$(
    cd $(dirname $0)
    pwd
)
# 进入项目路径下
cd ${BASE_DIR}

yarn run build
hexo d
if [ $? != 0 ]; then
    echo "构建失败,退出"
    exit -1
fi

# 拷贝项目路径下 themes/matery/source  到 oss 上去,bukect 替换你 自己的 oss bueket 名称

/Users/zhangpanqin/app/oss/ossutilmac64 cp -rf ${BASE_DIR}/themes/matery/source oss://bukect --meta=Cache-Control:public,max-age=2592000

if [ $? != 0 ]; then
    echo "上传 oss 失败,退出"
    exit -1
fi

public=${BASE_DIR}/public

if [ -d ${public} ]; then
    scp -rp ${public}/* 用户名@ip:/usr/share/nginx/html/
    echo "部署成功"
else
    echo "${public} 不存在,部署失败"
fi
```

我自己写的 shell 脚本，一直在用。

你只需将 `bucket` 配置你的 bucket 和 oss 配置文件就行。你运行 `ossutilmac64` 会提示你配置秘钥。

用户名一定要配置 ssh ，修改你自己的 ip。

然后 `chmod 744 ./deploy.sh` 让脚本文件可执行。

