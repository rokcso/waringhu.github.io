---
title: "Windows 10 提示管理员已阻止你运行此应用"
date: 2021-03-30T19:20:44+08:00
draft: false
slug: "windows-admin-block"
tags:
    - 计算机基础技能
---

# 案发现场

这个问题是发生在我安装 LoadRunner-11 的过程中，右键「以管理员身份运行」时出现如下弹窗提示。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330191830214-280698619.png)

# 解决方案

1. 找到不能成功以管理员身份运行的程序，按住 `Shift` 键的同时，鼠标右键单击该程序，点击`复制为路径`。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330191846204-1517193904.png)

2. 同时点击 `Win` + `S`，在左下角输入框里输入 `cmd`，如图点击`以管理员身份运行` cmd。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330191900695-1060368196.png)

3. 将刚刚（第 1 步）复制的路径粘贴到 cmd 里，然后点击回车运行。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330191911515-1252696575.png)

4. LoadRunner 成功以管理员身份运行。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330191921680-1468625106.png)

# 总结

同样的方式，也可以用在其他应用程序不能以管理员身份运行的情况下。