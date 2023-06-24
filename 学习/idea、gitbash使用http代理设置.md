---
layout: post
title:  给 Windows 的终端Terminal 配置代理
categories: [开发工具,git]
tags:  git
author: 归零叔
index_img: https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920154754068.png
---

# ![image-20200920154754068](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/image-20200920154754068.png)

# 给 Windows 的终端配置代理

### 缘起

之前遇到在 Windows 下给终端（cmd，Git Bash，PowerShell）配置代理时，总是模模糊糊的就过去了，今天又折腾了一次，恰巧有时间记下来，不想要再次重复了。



其实命令很简单，跟在 **Linux** 下没什么区别。

```
set http_proxy=http://127.0.0.1:1080

set https_proxy=http://127.0.0.1:1080

set http_proxy_user=user
set http_proxy_pass=pass

set https_proxy_user=user
set https_proxy_pass=pass

# 恢复
set http_proxy=

set https_proxy=

# Ubuntu 下命令为 export
# export http_proxy=http://127.0.0.1:1080
# 要取消该设置：
#unset http_proxy
#unsethttps_proxy
```

就是两条命令，前两条。

### 要点

1. 一定要加 `http://`，直接写域名或者 IP 不行。
2. **http** 和 **https** 都要设置。

然后如果想验证是否成功配置了代理的话，用 `ping` 命令是不可以的

### ping 还是不行的原因

ping的协议不是https，也不是https，是ICMP协议。

### 验证方式

`curl -vv http://www.google.com`，用这条命令来验证，如果返回如下结果表示代理设置成功。

![curl-google](https://blog-hexo-python.oss-cn-beijing.aliyuncs.com/markdown/curl-google.png)

这里还有一个坑是，**cmd**，**Git Bash**，**PowerShell** 设置的方式不同！！！有点精神分裂了。。。

- **cmd** 中用 `set http_proxy` 设置

- **Git Bash** 中用 `export http_proxy` 设置

- **PowerShell** 中按照这样设置

  ```
  # NOTE: registry keys for IE 8, may vary for other versions
  $regPath = 'HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings'
  
  function Clear-Proxy
  {
      Set-ItemProperty -Path $regPath -Name ProxyEnable -Value 0
      Set-ItemProperty -Path $regPath -Name ProxyServer -Value ''
      Set-ItemProperty -Path $regPath -Name ProxyOverride -Value ''
  
      [Environment]::SetEnvironmentVariable('http_proxy', $null, 'User')
      [Environment]::SetEnvironmentVariable('https_proxy', $null, 'User')
  }
  
  function Set-Proxy
  {
      $proxy = 'http://example.com'
  
      Set-ItemProperty -Path $regPath -Name ProxyEnable -Value 1
      Set-ItemProperty -Path $regPath -Name ProxyServer -Value $proxy
      Set-ItemProperty -Path $regPath -Name ProxyOverride -Value '<local>'
  
      [Environment]::SetEnvironmentVariable('http_proxy', $proxy, 'User')
      [Environment]::SetEnvironmentVariable('https_proxy', $proxy, 'User')
  }
  ```

**纠结于应该用 `set` 还是 `export` 还有一个判断方法是，敲一下这两个命令，如果返回一个长长的列表，就表示应该用这个命令，反之，如果返回找不到这个命令，就不应该用这个命令。**

### 总结

这次应该是搞清楚了 Windows 下如何给 **Terminal** 设置代理，花了一个多小时的时间，感觉很值！