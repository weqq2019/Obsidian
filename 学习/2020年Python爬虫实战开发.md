---
layout: post
title: 2020年Python爬虫实战开发
categories: [Python爬虫]
tags: python爬虫 
author: 归零叔
date: 2020/12/17 20:46:25
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201010172623506.png
---

{% note success  %}

#  第一章 : 爬虫基础简介

{% endnote %}

{% note secondary %}
## 1.1 爬虫初识&价值探讨
{% endnote %}

{% note light %}
**前戏**:

亲爱的观众朋友们：

- 你是否在夜深人静的时候,想看一些会让你更睡不着的图片却苦于没有资源...
- 你是否在节假日出行高峰的时候,想快速抢购火车票成功...
- 你是否在网上购物的时候,想快速且精准的定位到口碑质量最好的商品...
- 你是否想在考试或者面试前夕,想看一些具有针对性的题目和面试题....
- 你是否想在杂乱的网络世界中获取你想要的数据...

**什么是爬虫** :

- 形象概念： 爬虫，即网络爬虫，大家可以理解为在网络上爬行的一直蜘蛛，互联网就比作一张大网，而爬虫便是在这张网上爬来爬去的蜘蛛咯，如果它遇到资源，那么它就会抓取下来。想抓取什么？这个由你来控制它。

- 学术概念：爬虫就是通过编写程序**模拟**浏览器上网，让其去互联网上**抓取**数据的过程。

**爬虫的价值**

​		  之前在授课过程中,好多同学都问过我这样的一个问题:为什么要学习爬虫,学习爬虫能够为我们以后的发展带来哪些好处？其实学习爬虫的原因和为我们以后发展带来的好处都是显而易见的,无论是从实际的应用还是从就业上.

​		  爬取互联网上的数据,为我所用,有了大量的数据,就如同有了一个数据银行一样,下一步做的就是如何将这些爬虫的数据产品化,商业化.

![image-20201010181042070](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201010181042070.png)

​		  从就业的角度来说,爬虫工程师目前来说属于紧缺人才,并且薪资待遇普遍较高所以,深层次地掌握这门技术,对于就业来说,是非常有利的.有些人学习爬虫可能为了就业或者跳槽.从这个角度来说,爬虫工程师是不能的选择之一.随着大数据时代的来临,爬虫技术的应用将来越广泛,在未来会拥有更好的发展空间.

{% endnote %}

{% note secondary %}
## 1.2 爬虫合法性探究
{% endnote %}

{% note light %}

**正解在此**

爬虫作为一种计算机技术就决定了它的**中立性**，因此爬虫本身**在法律上并不被禁止**，但是利用爬虫技术获取数据这一行为是具有违法甚至是犯罪的风险的。所谓具体问题具体分析，正如水果刀本身在法律上并不被禁止使用，但是用来捅人，就不被法律所容忍了。

或者我们可以这么理解：爬虫是用来批量获得网页上的公开信息的，也就是前端显示的数据信息。因此，既然本身就是公开信息，其实就像浏览器一样，浏览器解析并显示了页面内容，爬虫也是一样，只不过爬虫会批量下载而已，**所以是合法的**。不合法的情况就是配合爬虫，利用黑客技术攻击网站后台，窃取后台数据（比如用户数据等）。

举个例子：像谷歌百度这样的搜索引擎爬虫，每隔几天对全网的网页扫一遍，供大家查阅，各个被扫的网站大都很开心。这种就被定义为“善意爬虫”。但是像抢票软件这样的爬虫，对着 12306 每秒钟恨不得撸几万次，铁总并不觉得很开心，这种就被定义为“恶意爬虫”。

**爬虫所带来风险主要体现在以下2个方面：**

- 爬虫干扰了被访问网站的正常运营；
- 爬虫抓取了受到法律保护的特定类型的数据或信息。

**那么作为爬虫开发者，如何在使用爬虫时避免进局子的厄运呢？**

- 严格遵守网站设置的robots协议；
- 在规避反爬虫措施的同时，需要优化自己的代码，避免干扰被访问网站的正常运行；
- 在使用、传播抓取到的信息时，应审查所抓取的内容，如发现属于用户的个人信息、隐私或者他人的商业秘密的，应及时停止并删除。



可以说在我们身边的网络上已经密密麻麻爬满了各种网络爬虫，它们善恶不同，各怀心思。而越是每个人切身利益所在的地方，就越是爬满了爬虫。**所以爬虫是趋利的，它们永远会向有利益的地方爬行。**技术本身是无罪的，问题往往出在人无限的欲望上。因此爬虫开发者的道德自持和企业经营者的良知才是避免触碰法律底线的根本所在。

{% endnote %}

{% note secondary %}

## 1.3 爬虫初始深入

{% endnote %}

{% note light %}

**哪些语言可以实现爬虫**

- `php`: 可以实现爬虫,php称号称是全世界最优美的语言(当然是其自己号称的,就是王婆卖瓜的意思) . 但是php在实现爬虫中支持多线程和多进程方面排行的不好 .
- `c、c++`: 可以实现爬虫,但是使用这种方式实现爬虫纯粹是某些人(大佬们)能力的体现,却不是明智和合理的选择 .
- `java`: 可以实现爬虫 . java可以非常好的处理和实现爬虫 . 是唯一可以与python驾齐驱且是python的头号劲敌 . 但是java实现爬虫代码较为臃肿 , 重构成本较大 .
- `python`: 可以实现爬虫 . python实现和处理语法简单 , 代码优美 , 支持的模块繁多 , 学习成本低 , 具有非常强大的框架且一语难以言表的好！没有但是！

**爬虫在使用场景中的分类**

- 通用爬虫
  - 通用爬虫是搜索引擎(`Baidu`、`Google`、`Yahoo`) “爬取系统”的重要组成部分 . 主要目的是将互联网上的网页下载到本地 , 形成一个互联网内容的镜像备份 . 简单来说就是尽可能的 ；把互联网上的所有网页下载下来,放到本地服务器形成备份,在对这些网页做相关处理(提取关键字、去掉广告),最后提供一个用户检索接口 .
  - 抓取系统重要组成部分 . 抓取的是一整张页面数据 .
- 聚焦爬虫
  - 聚焦爬虫是根据指定的需求爬取网络上指定的数据 . 例如:获取豆瓣上电影的名称和影评 , 而不是获取整张页面中所有的数据值 .
  - 是建立在通用爬虫的基础之上 . 抓取的是页面中特定的局部内部 .
- 增量式爬虫
  - 增量式是用来检测网站数据更新的情况 , 且可以将网站更新的数据进行爬取 ( 后期会有章节单独对其展详细讲解 )

**爬虫的矛和盾**

- 有一个说法的是,互联网上50%的流量都是爬虫创造的 . 这个说法虽然夸张了点 ,但也体现出了爬虫的无处不在 . 爬虫之所以无所不在 , 是因为爬虫可以为互联网企业带来收益 .
- 对于先关的电商网站来说 , 很多电商网站是愿意被比价网站或者其他购物信息网站爬取信息的 , 因为这样能够给他们的商品带来更多流量 . 但他们不愿意被其他电商网站获取价格信息和商品描述 , 因为担心其他电商恶意比价或进行抄袭 . 同时他们又经常去爬其他电商网站的数据 , 希望能够看到别人的价格 .

![image-20201011093917171](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201011093917171.png)

- 这种纠结又复杂的心情像学霸间的竞争 , 学霸可以给学渣抄笔记 , 因为知道学渣再怎么努力也就是六七分的水平 , 但学霸对其他学霸一定会严防死守 , 因为只有学霸和学霸之间才有真正的竞争 . 那么这种矛盾如何被解决呢？

**反爬机制**

- 门户网站通过制定相应的策略和技术手段 , 防止爬虫程序进行网站数据的爬取 .

**反反爬策略**

- 爬虫程序通过相应的策略和技术手段 , 破解门户网站的反爬虫手段 , 从而爬取到相应的数据 .

**robots协议**

- 几乎和爬虫技术诞生的同一时刻 , 反爬虫技术也诞生了 .在90年代开始有搜索引擎网站利用爬虫技术爬取网站时 , 一些搜索引擎从业者和网站站长通过邮件讨论定了一项 “ 君子协议 ” —— robots.txt . 即网站有权规定网站中哪些内容可以被爬虫爬取 , 哪些内容不可以被爬虫抓取 . 这样即可以保护隐私和敏感信息 , 又可以被搜索引擎收录 、 增加流量 .
- 历史上第一桩关于爬虫的官司诞生在2000年 , eBay将一家聚合价格信息的比价网站BE告上了法院 . eBay声称自己已经将哪些信息不能抓取写进了robots协议中 , 但BE违反了这一协议 . 但BE认为eBay上的内容属于用户集体贡献而不归用户所有 , 爬虫协议不能用作法律参考 . 最近经过业内反复讨论和法庭上的几轮唇枪舌战 , 最终以eBay胜诉告终 ,也开了用爬虫robots协议作为主要参考的先河 .
- 最后,可以通过网站域名+/robots.txt的形式访问该网站的协议详情 . 例如:www.taobao.com/robots.txt

{% endnote %}

{% note secondary %}

## 1.4 http&https协议

{% endnote %}

{% note light %}

- **http协议**
  - 概念 : HTTP协议是Hyper Text Transfer Protocol ( 超文本传输协议 )的缩写 , 是用于从万维网 ( WWW:World Wide Web ) 服务器传输超文本到本地浏览器的传送协议 . (虽然童鞋们将这条概念都看烂了 ,但是也没办法 , 毕竟这就是HTTP的权威官方的概念解释 , 想要彻底理解 , 请客观目移下侧.....)
  - 白话概念 : HTTP协议就是服务器(Server)和客户端(Client) 之间进行数据交互 ( 互相传输数据 ) 的一种形式 . 我们可以将Server和Client进行拟人化 , 那么该协议就是Server和Client这两兄弟间指定的一种交互沟通方式.大家都过智取威虎山中场子荣和土匪之间的黑话吧:

``` 
　　　　　　- 土匪：蘑菇，你哪路？什么价？（什么人？到哪里去？）
　　　　　　- 杨子荣：哈！想啥来啥，想吃奶来了妈妈，想娘家的人，孩子他舅舅来了。（找同行）
　　　　　　- 杨子荣：拜见三爷！
　　　　　　- 土匪：天王盖地虎！（你好大的胆！敢来气你的祖宗？）
　　　　　　- 杨子荣：宝塔镇河妖！（要是那样，叫我从山上摔死，掉河里淹死。）
　　　　　　- 土匪：野鸡闷头钻，哪能上天王山！（你不是正牌的。）
　　　　　　- 杨子荣：地上有的是米，喂呀，有根底！（老子是正牌的，老牌的。）
　　　　　　- 土匪：拜见过阿妈啦？（你从小拜谁为师？）
　　　　　　- 杨子荣：他房上没瓦，非否非，否非否！（不到正堂不能说。）
　　　　　　- 土匪：嘛哈嘛哈？（以前独干吗？）
　　　　　　- 杨子荣：正晌午说话，谁还没有家？（许大马棒山上。）
　　　　　　- 土匪：好叭哒！（内行，是把老手）
　　　　　　- 杨子荣：天下大耷拉！（不吹牛，闯过大队头。）
　　　　　　- 座山雕：脸红什么？
　　　　　　- 杨子荣：精神焕发！
　　　　　　- 座山雕：怎么又黄了？
　　　　　　- 杨子荣：防冷，涂的蜡！
　　　　　　- 座山雕：晒哒晒哒。（谁指点你来的？）
　　　　　　- 杨子荣：一座玲珑塔，面向青寨背靠沙！（是个道人。）
```

是不是看到这里,有得童鞋终于知道了传说的中的‘天王盖地虎’是真正含义了吧 .此黑话其实就是杨子荣和土匪之间进行交互沟通的方式 (协议).

- **HTTP工作原理**

  - HTTP协议工作于客户端-服务端架构为上 . 浏览器作为HTTP客户端通过URL向HTTP服务器即WEB服务器发送所有请求.Web服务器根据接收到的请求后,向客户端发送响应信息 . 

  ![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/snip20190410_8.png)
  
- 请求头信息

```python
　　　　　　　　accept:"浏览器通过这个头告诉服务器，它所支持的数据类型"
　　　　　　　　Accept-Charset: "浏览器通过这个头告诉服务器，它支持哪种字符集"
　　　　　　　　Accept-Encoding："浏览器通过这个头告诉服务器，支持的压缩格式"
　　　　　　　　Accept-Language："浏览器通过这个头告诉服务器，它的语言环境"
　　　　　　　　Host："浏览器通过这个头告诉服务器，想访问哪台主机"
　　　　　　　　If-Modified-Since: "浏览器通过这个头告诉服务器，缓存数据的时间"
　　　　　　　　Referer："浏览器通过这个头告诉服务器，客户机是哪个页面来的 防盗链"
　　　　　　　　Connection："浏览器通过这个头告诉服务器，请求完后是断开链接还是何持链接"
　　　　　　　　X-Requested-With: "XMLHttpRequest 代表通过ajax方式进行访问"
　　　　　　　　User-Agent："请求载体的身份标识"
```

- 响应头信息

```shell
　　　　　　　　　　　　Location: 服务器通过这个头，来告诉浏览器跳到哪里
　　　　　　　　　　　　Server：服务器通过这个头，告诉浏览器服务器的型号
　　　　　　　　　　　　Content-Encoding：服务器通过这个头，告诉浏览器，数据的压缩格式
　　　　　　　　　　　　Content-Length: 服务器通过这个头，告诉浏览器回送数据的长度
　　　　　　　　　　　　Content-Language: 服务器通过这个头，告诉浏览器语言环境
　　　　　　　　　　　　Content-Type：服务器通过这个头，告诉浏览器回送数据的类型
　　　　　　　　　　　　Refresh：服务器通过这个头，告诉浏览器定时刷新
　　　　　　　　　　　　Content-Disposition: 服务器通过这个头，告诉浏览器以下载方式打数据
　　　　　　　　　　　　Transfer-Encoding：服务器通过这个头，告诉浏览器数据是以分块方式回送的
　　　　　　　　　　　　Expires: -1 控制浏览器不要缓存
　　　　　　　　　　　　Cache-Control: no-cache 
　　　　　　　　　　　　Pragma: no-cache
```



- **常用请求头信息**
  - User-Agent："请求载体的身份标识"
  - Connection："浏览器通过这个头告诉服务器，请求完后是断开链接还是何持链接"
- **常用响应头信息**
  - Content-Type：服务器通过这个头，告诉浏览器回送数据的类型
- **https协议**

![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/snip20190410_3.png)

- **加密方式**

  - 对称秘钥加密

    客户端向服务器发送一条信息，首先客户端会采用已知的算法对信息进行加密，比如MD5或者Base64加密，接收端对加密的信息进行解密的时候需要用到密钥，中间会传递密钥，（加密和解密的密钥是同一个），密钥在传输中间是被加密的。这种方式看起来安全，但是仍有潜在的危险，一旦被窃听，或者信息被挟持，就有可能破解密钥，而破解其中的信息。因此“共享密钥加密”这种方式存在安全隐患。

  ![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/snip20190410_5.png)

  - 非对称秘钥加密

    “非对称加密”使用的时候有两把锁，一把叫做“私有密钥”，一把是“公开密钥”，使用非对象加密的加密方式的时候，服务器首先告诉客户端按照自己给定的公开密钥进行加密处理，客户端按照公开密钥加密以后，服务器接受到信息再通过自己的私有密钥进行解密，这样做的好处就是解密的钥匙根本就不会进行传输，因此也就避免了被挟持的风险。就算公开密钥被窃听者拿到了，它也很难进行解密，因为解密过程是对离散对数求值，这可不是轻而易举就能做到的事。以下是

    ![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/snip20190410_6.png)

    但是非对称秘钥加密技术也存在如下缺点：

    - 第一个是：如何保证接收端向发送端发出公开秘钥的时候，发送端确保收到的是预先要发送的，而不会被挟持。只要是发送密钥，就有可能有被挟持的风险。
    - 第二个是：非对称加密的方式效率比较低，它处理起来更为复杂，通信过程中使用就有一定的效率问题而影响通信速度

  - 证书秘钥加密

    在上面我们讲了非对称加密的缺点，其中第一个就是公钥很可能存在被挟持的情况，无法保证客户端收到的公开密钥就是服务器发行的公开密钥。此时就引出了公开密钥证书机制。数字证书认证机构是客户端与服务器都可信赖的第三方机构。证书的具体传播过程如下：

    - 服务器的开发者携带公开密钥，向数字证书认证机构提出公开密钥的申请，数字证书认证机构在认清申请者的身份，审核通过以后，会对开发者申请的公开密钥做数字签名，然后分配这个已签名的公开密钥，并将密钥放在证书里面，绑定在一起
    - 服务器将这份数字证书发送给客户端，因为客户端也认可证书机构，客户端可以通过数字证书中的数字签名来验证公钥的真伪，来确保服务器传过来的公开密钥是真实的。一般情况下，证书的数字签名是很难被伪造的，这取决于认证机构的公信力。一旦确认信息无误之后，客户端就会通过公钥对报文进行加密发送，服务器接收到以后用自己的私钥进行解密。

  ![img](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/snip20190410_7.png)

  ![image-20201015091705530](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20201015091705530.png)

{% endnote %}

{% note success  %}

#  第二章 : requests模块基础

{% endnote %}

{% note secondary %}

## 1.1 requests第一血

{% endnote %}

{% note light %}

requests模块

- urllib模块
- requests模块

**为什么要使用requests模块**

- 在使用urllib模块的时候，会有诸多不便之处，总结如下：
  - 手动处理url编码
  - 手动处理post请求参数
  - 处理cookie和代理操作繁琐
  - ……
- 使用requests模块：
  - 自动处理url编码
  - 自动处理post请求参数
  - 简化cookie和代理操作
  - ……



**requtests模块**:python中原生的一款基于网络请求的模块,功能非常强大,简单便捷,效率极高.

- 作用:	模拟浏览器发请求.
- 使用:   

  - 环境安装
    - pip install requests
  - 使用流程/编码流程
    - 指定url
    - 发起请求
    - 获取响应数据
    - 持久化存储
  - 实战编码
    - 需求:爬取搜狗首页的页面数据

  ## **第一个爬虫程序**

  - **需求：爬取搜狗首页的页面数据**

  ```python
  
  # -*- coding: utf-8 -*-
  # __author__:归零叔
  # 2020/12/16 下午11:14
  # - 需求:爬取搜狗首页的页面数据
  import requests
  if __name__ == '__main__':
  #1:指定url
  url='https://www.sogou.com/'
  #2:发起请求
  #get方法会返回一个响应对象
  response=requests.get(url=url)
  #3.获取响应数据.text返回的是字符串形式的响应数据
  page_text=response.text
  print(page_text)
  #4.持久化存储
  with open('./sogou.html','w',encoding='utf-8') as fp:
  fp.write(page_text)
  print('爬取数据结束！！！')
  ```

  - 实战巩固

    - 需求: 爬取搜狗指定词条对应的搜索结果页面(简易网页采集器)

      - UA检测
      - UA伪装

      ```python
      # -*- coding: utf-8 -*-
      # __author__:归零叔
      # 2020/12/16 下午11:46
      # - 需求: 简易网页采集器
      
      #UA伪装：门户网站的服务器会检测对应请求的载体身份标识，如果检测到请求的载体身份标识为某一款浏览器，
      #UA:User-Agent(请求载体的身份标识)
      #说明该请求是一个正常的请求。但是，如果检测到请求的载体身份标识不是基于某一款浏览器，则表示该请求为不正常的请求（爬虫），则服务器端就很有可能拒绝该次请求。
      
      #UA伪装：让爬虫对应的请求载体身份标识伪装成某一款浏览器
      import requests
      if __name__ == '__main__':
      #UA伪装：将对应的User-Agent封装到字典中
      headers={
      'User-Agent':'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.88 Safari/537.36'
      }
      url='https://www.sogou.com/web'
      #处理url携带的参数:封装到字典中
      kw=input("enter a word:")
      param={
      'query':kw
      }
      #对指定的url发起的请求对应的url最携带的参数，并且请求过程中处理了参数
      response=requests.get(url=url,params=param,headers=headers)
      
      page_text=response.text
      filename=kw+'.html'
      
      with open (filename,'w') as fp:
      fp.write(page_text)
      print(filename,'保存成功')
       
      ```

    - 需求: 破解百度翻译

      - post请求 ( 携带了参数)

      - 响应数据是一组json数据 

        ```python
        # -*- coding: utf-8 -*-
        # __author__:归零叔
        # 2020/12/17 下午4:41
        # - 需求:百度翻译
        
        import requests
        import json
        
        if __name__ == '__main__':
        # 1.指定url
        post_url = 'https://fanyi.baidu.com/sug'
        # 2.进行UA伪装
        headers = {
        'User-Agent': 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.88 Safari/537.36'
        }
        # 3.post请求参数处理（同get请求一致)
        word=input('enter a word:')
        data = {
        'kw': word
        }
        # 4.请求发送
        response = requests.post(url=post_url, data=data, headers=headers)
        # 5.获取响应数据:json()方法返回的是obj （如果确认响应数据是json类型，才可以使用json()）
        dic_obj = response.json()
        
        #持久化存储
        fileName=word+'.josn'
        fp=open(fileName,'w',encoding='utf-8')
        json.dump(dic_obj,fp=fp,ensure_ascii=False)
        print('over!!!')
        ```

        

    - 需求: 爬取豆瓣电影分类排行榜 https://moive.douban.com/中的电影详情数据

      ```python
      # -*- coding: utf-8 -*-
      # __author__:归零叔
      # 2020/12/17 下午5:44
      # - 需求: 豆瓣电影爬取
      
      import requests
      import json
      
      if __name__ == '__main__':
      url = 'https://movie.douban.com/j/chart/top_list'
      param = {
      'type': '24',
      'interval_id': '100:90',
      'action': '',
      'start': '0',
      'limit': '20'
      }
      headers = {
      'User-Agent': 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.88 Safari/537.36'
      }
      response = requests.get(url=url, params=param, headers=headers)
      
      list_data=response.json()
      
      fp=open('./douban.json','w',encoding='utf-8')
      json.dump(list_data,fp=fp,ensure_ascii=False)
      
      print('over!!!')
      ```

      

    - 需求(作业): 爬取肯德基厅查询http://www.kfc.com.cn/kfccda/index.aspx中指定地点的餐厅位置

      ```python
      # -*- coding: utf-8 -*-
      # __author__:归零叔
      # 2020/12/17 下午6:38
      # - 需求: KFC指定的地点爬取
      
      import requests
      
      if __name__ == '__main__':
      #1.指定url
      post_url='http://www.kfc.com.cn/kfccda/ashx/GetStoreList.ashx?op=keyword'
      
      #2.UA伪装
      headers = {
      'User-Agent': 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/87.0.4280.88 Safari/537.36'
      }
      
      #3.post发起请求
      word=input('enter 一个地点:')
      data={
      'cname':'',
      'pid':'',
      'keyword':word,
      'pageIndex':'1',
      'pageSize':'10'
      }
      response=requests.post(url=post_url,data=data,headers=headers)
      
      #4.获取响应数据
      page_text=response.text
      
      #4.持久化存储
      fileName=word+'.html'
      with open(fileName,'w',encoding='utf-8') as fp:
      fp.write(page_text)
      print('over!!!')
      
      ```
      
    - 需求: 爬取国家药品监督管理总局中基于中华人民共和国化妆品生产许可证相关数据

      - 动态加载数据

      - 首页中 对应的企业信息数据是通过ajax动态请求到的.

      - 通过对详情页url的观察发现:

        http://scxk.nmpa.gov.cn:81/xk/itownet/portal/dzpz.jsp?id=d4a427aef28343b0804319d7299797a8

        http://scxk.nmpa.gov.cn:81/xk/itownet/portal/dzpz.jsp?id=7027eb13f37a42c8803b28cad408d05d

      - url的域名是一样的,只有携带的参数(ID)不一样

      - ID值可以从首页对应的ajax请求到的json串中获取

      - 域名和id值拼接处一个完整的企业对应的详情页的url

    - 详情页的企业详情数据也是动态加载出来的

      - http://scxk.nmpa.gov.cn:81/xk/itownet/portalAction.do?method=getXkzsById

{% endnote %}

