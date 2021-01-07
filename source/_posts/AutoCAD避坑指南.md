---
title: "Auto CAD 避坑指南"
tags:
  - Auto CAD
  - 问题复盘
categories: 
- 问题复盘
date: 2021-01-07 18:39
---

前两天给舍友重装AutoCAD出了一些岔子，耽误了不少功夫，总结一下，以后避坑用。

> ## 一号坑：将AutoCAD移动至其他盘符下

### 问题描述

因为一些需求需要将AutoCAD从原安装位置移动至其他盘符下。

### 解决方案

移你马，移动了以后可能导致一堆问题和屁事，不一定能解决还耽误时间 ，使用Geek Uninstaller或者卸载工具卸载干净后重新安装就完了。卸载后重装可能出现的相关问题见下文。

> ## 二号坑：AutoCAD2020卸载后无法重装

### 问题描述

将AutoCAD2020卸载后，重新安装过程中，安装软件提示已经安装完成，但实际上并未安装。

### 解决方案

1. 打开注册表编辑器
2. 进入`HKEY_LOCAL_MACHINE\SOFTWARE`目录
3. 删除`Autodesk`注册表项
4. 进入`HKEY_LOCAL_MACHINE\SOFTWARE`目录
5. 删除`Autodesk`注册表项
6. 按照三号坑中解决方案处理一遍注册表项

> ## 三号坑：AutoCAD2020卸载后重装提示安装未完成

### 问题描述

将AutoCAD2020卸载后，重新安装至最后一个产品时提示“安装未完成，某些产品无法安装”。

![autocad安装未完成](https://gitee.com/qianshanyao/image-bed/raw/master/my_blog/AutoCad2020Error1603.png)

### 解决方案

1. 打开注册表编辑器
2. 进入`HKEY_CLASSES_ROOT\Installer\Products`目录
3. 删除所有`FEE98`开头的注册表项