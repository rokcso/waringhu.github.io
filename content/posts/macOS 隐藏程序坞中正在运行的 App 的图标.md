---
title: "macOS 隐藏程序坞中正在运行的 App 的图标"
date: 2023-05-08T10:07:55+08:00
draft: false
slug: "Hide the icon of the running App in the macOS program dock"
tags:
    - 技巧
---

2023-05-10 15:02 更新：如下操作之后当时钉钉可正常启动、使用，但是今天发现无法正常启动，不建议再使用以下方式。

> 操作环境：macOs Ventura 13.3.1 (a) (22E772610a)

如下图，钉钉为正在运行中的 App，其图标显示在 macOS 程序坞中，但是我希望将其图标隐藏。

![image-20230508095242443](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/image-20230508095242443.png)

即 App 保持运行中但是不在程序坞中显示 App 图标。这里仅推荐修改 App `Info.plist` 一种方式。

据网上其他用户的分享，该方式可能导致 App 无法正常运行，可实际尝试后判断是否使用该方式。

# 具体实现

在 Finder 中「应用程序」文件夹下找到「钉钉.app」，点击右键选择「显示包内容」，点击「Contents」，找到「Info.plist」文件并打开。

![image-20230508095914499](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/image-20230508095914499.png)

在 `<dict>` 中添加如下两行代码：

```
<key>LSUIElement</key>
<string>1</string>
```

![image-20230508100021611](https://waringhu-md-img-oss.oss-cn-hangzhou.aliyuncs.com/md-img/image-20230508100021611.png)

保存 `Info.plist` 后重启钉钉 App。

完成，此时钉钉正在运行中，但是程序坞中并无其 App 图标。

如果在修改 `Info.plist` 文件后重启钉钉 App 提示应用程序无法打开，则可以删除 `Info.plist` 文件中添加的代码后重启钉钉 App 并在退出钉钉 App 后重新向 `Info.plist` 中添加代码后重启钉钉 App。