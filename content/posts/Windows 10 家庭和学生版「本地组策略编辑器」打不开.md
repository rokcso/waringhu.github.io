---
title: "Windows 10 家庭和学生版「本地组策略编辑器」打不开"
date: 2021-03-30T18:59:50+08:00
draft: false
slug: "windows-local-group"
tags:
    - 计算机基础技能
---

1. 在桌面点击鼠标右键，选择新建，点击文本文档。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330184837932-1710594503-20230629161854527.png)

2. 不需要命名，直接打开新建的文本文档，复制粘贴以下内容，保存然后关闭该文本文档

```
@echo off

pushd "%~dp0"

dir /b C:\Windows\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~3*.mum >List.txt

dir /b C:\Windows\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~3*.mum >>List.txt

for /f %%i in ('findstr /i . List.txt 2^>nul') do dism /online /norestart /add-package:"C:\Windows\servicing\Packages\%%i"

pause
```

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330184900169-849110347.png)

3. 将该文本文档文件扩展名改为 `.cmd`。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330184915036-2087837800.png)

4. **以管理员身份运行**该 `cmd` 文件。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330184926356-2115979610.png)

5. 等待 cmd 程序运行，直到提示`操作成功完成，请按任意键继续...`

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330184937710-2008615392.png)

6. 按下 `Win` + `R` 组合键打开运行工具，输入 `gpedit.msc`，回车运行（或点击`确定`）。

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330184955869-197266587.png)

7. 成功打开「本地组策略编辑器」

![](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/2341884-20210330185007305-1972286635.png)