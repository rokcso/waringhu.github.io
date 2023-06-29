---
title: "Windows 10 已经连接网络，但是浏览器仍提示「未连接到互联网」"
date: 2021-05-10T11:20:23+08:00
draft: false
slug: "windows10-network"
tags:
    - 计算机基础技能
---

# 案发现场

Windows 已经连接网络，且显示 Internet 访问，但是使用浏览器访问网页却提示「未连接到互联网」，大概率是代理服务器的问题。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210510111709565-1782240937.png)

# 解决办法

1. 打开「控制面板」，点击进入「网络和 Internet」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210510111828735-1916703108.png)

2. 点击进入「Internet 选项」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210510111839728-178481523.png)

3. 点击「连接」，然后点击进入「局域网设置」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210510111855195-1274049855.png)

4. 找到「代理服务器」，取消勾选

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210510111907984-559885066.png)

5. 然后一路确定，浏览器刷新，问题已经解决