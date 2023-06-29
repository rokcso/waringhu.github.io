---
title: "破解 LoadRunner-11 时添加 New License 出错"
date: 2021-03-30T19:49:04+08:00
draft: false
slug: "loadrunner11-new-license"
tags:
    - 计算机基础技能
---

# ERROR-1

Cannot save the license information because access to the registry is denied. Please provide the current user with write permission for the HKEY_LOCAL_MACHINE registry key.

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330194848450-2043979266.png)

# 解决方案：

以管理员身份运行 LoadRunner，然后再添加 New License。

如果不能顺利地以管理员身份运行，请参考：[【解决】Win 10 提示管理员已阻止你运行此应用](https://blog.waringhu.com/post/2021/03/windows-admin-block/)

# ERROR-2

Invalid license key.

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210331095113195-1869961744.png)

重新复制粘贴替换 LoadRunner 安装位置 `HP\LoadRunner\bin` 文件夹下的  `lm70.dll` 和 `mlr5lprg.dll` 这两个文件。

再次**以管理员身份运行** `deletelicense.exe` 文件。

**以管理员身份运行** LoadRunner，然后重新添加许可证密钥。