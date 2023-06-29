---
title: "Windows 10 Microsoft Store 无法连接网络"
date: 2021-05-19T20:01:45+08:00
draft: false
slug: "microsoft-store-network"
tags:
    - 计算机基础技能
---

# 案发现场

网络连接正常，浏览器网页均可刷新。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210519195902122-577015917.png)

# 解决方案

一共有两种办法，都试试应该能成功（至少我成功了）。

## ROUND-1

1. 打开「控制面板」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210519195913271-250354905.png)

2. 点击「网络和 Internet」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210519195924573-227584792.png)

3. 点击「Internet 选项」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210519195935534-1209710164.png)

4. 点击「高级」，找到如图与「TLS」有关的选项，全部勾选上，点击「应用」或者「确定」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210519195946454-1821465801.png)

## ROUND-2

1. 右击「网络」，点击「打开"网络和 Internet"设置」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210519195956092-730895085.png)

2. 点击「代理」，关闭「自动检测设置」、「使用设置脚本」和「使用代理服务器」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210519200004252-1626591938.png)

# 结

至此，我的 Microsoft Store 已经可以正常访问了，你的就不知道了。