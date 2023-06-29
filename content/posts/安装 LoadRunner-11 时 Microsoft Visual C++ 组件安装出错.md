---
title: "安装 LoadRunner-11 时 Microsoft Visual C++ 组件安装出错"
date: 2021-03-30T19:40:11+08:00
draft: false
slug: "loadrunner11-error"
tags:
    - 计算机基础技能
---

下面将我所有尝试过的方法都罗列了出来，如果一次不能成功还可以试试其他方法。

# ROUND-1

1. 打开 LoadRunnr-11 的文件夹，进入 `loadrunner-11\Additional Components\IDE Add-Ins\MS Visual Studio .NET`。
2. 运行 `LRVS2005IDEAddInSetup.exe`。
3. 再次安装 `loadrunner-11`。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330193931326-1961780710.png)

# ROUND-2

1. 打开 LoadRunnr-11 的文件夹，进入 `loadrunner-11\lrunner\Chs\prerequisites\vc2005_sp1_redist`。
2. 运行 `vcredist_x86.exe`。
3. 再次安装 `loadrunner-11`。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330193941354-558612736.png)

# ROUND-3

将 ROUND-2 里面的 `vcredist_x86.exe` 解压（如何解压 `.exe` 文件请自行搜索），在解压得到的 `vcredist_x86` 文件夹里找到 `VCREDI~3.EXE` 文件，运行该文件。

然后再次安装 `loadrunner-11`。