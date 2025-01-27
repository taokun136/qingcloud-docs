---
title: "卸载硬盘"
description: 本小节主要介绍云硬盘的卸载相关操作。
draft: false
enableToc: false
weight: 50
keyword: 云计算, 青云, QingCloud, 云硬盘, 卸载
---

本节旨在指导用户将挂载到云服务器的数据盘进行卸载。

## 前提条件

- 对于 Windows 云服务器，在线卸载云硬盘前，请确保没有程序正在对该云硬盘进行读写操作。否则，将造成数据丢失。
- 对于 Linux 云服务器，在线卸载云硬盘前，请先登录到云服务器，执行`umount`命令，取消待卸载云硬盘与文件系统之间的关联，并确保没有程序正在对该云硬盘进行读写操作。否则，卸载云硬盘将失败。

## 操作步骤

1. 登录管理控制台。

2. 在控制台导航栏中，选择**产品与服务** > **存储服务** > **云硬盘**，进入**硬盘**页面。

3. 在云硬盘列表右键点击需要卸载的硬盘，选择**卸载硬盘**。
   ![unload_1](/storage/disk/_images/unload_1.png)

4. 确认硬盘在云服务器操作系统中处于非挂载状态。在弹出的提示框中，点击**确认**。
   ![unload_2](/storage/disk/_images/unload_2.png)

5. 当云硬盘状态显示为“可用”时，表示已卸载成功。
   ![unload_3](/storage/disk/_images/unload_3.png)

