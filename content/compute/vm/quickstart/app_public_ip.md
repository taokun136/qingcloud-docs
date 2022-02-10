---
title: "步骤二：申请并绑定公网 IP（可选）"
description: 本章节介绍如何申请并绑定公网 IP
draft: false
weight: 20
keyword: 云计算, 青云, QingCloud, 云服务器，申请并绑定公网 IP
---

弹性公网 IP 是指将公网 IP 地址和云服务器绑定，以实现 VPC 内的云服务器通过固定的公网 IP 地址对外提供访问服务。

- 若创建云服务器时，您没有为云服务器绑定公网 IP 地址，且需要通过公网 IP 地址登录到云服务器，您可以参考本章节操作步骤申请并绑定公网 IP 地址。

- 若创建云服务器时，您已为云服务器绑定公网 IP 地址，可跳过此步骤。

## 前提条件

- 已获取管理控制台的账号和密码。
- 已创建云服务器。

## 操作步骤

1. 登录 QingCloud 管理控制台。

2. 选择**产品与服务** > **计算** > **云服务器**，进入云服务器列表页面。

   ![](../../_images/vm_server_list.png)

3. 在左侧导航栏中，选择**网络** > **公网 IP**，进入**公网 IP** 页面。

   ![](../../_images/vm_create_public_ip.png)

4. 点击**申请**，弹出**提示**窗口。

5. 提示信息阅读完后，点击**继续申请**，弹出**申请公网 IP** 窗口。

   <img src="../../_images/vm_create_public_ip_win.png" style="zoom:50%;" />

6. 根据需要配置相关参数。

7. 配置完成后，点击**提交**，完成公网 IP 的申请。

8. 在公网 IP 列表中，鼠标右键点击申请的公网 IP，在弹框中，点击**分配到云服务器**。

   ![](../../_images/vm_create_public_ip_assign.png)

9. 在弹出的选择绑定的云服务器窗口中，选择待绑定的云服务器。

   <img src="../../_images/vm_choose_vm.png" style="zoom:50%;" />

10. 点击**确认**，完成公网 IP 的绑定操作。

    私有网络内的负载均衡器或云服务器绑定了 EIP 后，外网访问将使用 EIP 作为进出网关。如果同时配置了 VPC 的端口转发规则，端口转发规则将不再有效。

11. 绑定完成后，在左侧导航栏中，选择**计算** > **云服务器**，在云服务器列表中，可查看绑定的公网 IP 地址。

    ![](../../_images/vm_vm_public_ip.png)