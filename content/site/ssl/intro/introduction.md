---
title: "SSL证书介绍"
date: 2020-12-01T00:38:25+09:00
description: ssl证书基本介绍
draft: false
enableToc: false
keyword: 云计算, 青云, QingCloud, ssl证书
weight: 2
---



QingCloud SSL 证书提供了安全套接层证书的一站式服务，包括证书申请,管理及部署功能,与 [亚洲诚信](https://www.trustasia.com/) 合作，提供完整的证书解决方案。

## 名词解释 {#id2}

**SSL 证书**

即安全套接层（SSL）数字证书，数字证书是一种用于电脑的身份识别机制。数字证书可以从身份认证机构获得。理论上任何人都可以颁发数字证书。颁发数字证书的个人或机构对公钥进行加签。一般国际可信的证书由 CA 机构制作颁发。

**HTTPS**

是一种网络安全传输协议。在计算机网络上，HTTPS 经由超文本传输协议进行通信，利用 SSL/TLS 来对数据包进行加密。HTTPS 开发的主要目的，是提供对网络服务器的身份认证，保护交换数据的隐私与完整性。

**CA机构**

数字证书授权机构 （Certificate Authority） 是负责发放和管理数字证书的权威机构。

## 证书类型 {#id3}


| 证书类型 | 域名型(DV)SSL证书 | 企业型(OV)SSL证书 | 企业增强型(EV)SSL证书 |
|:--- |:--- |:--- |:--- |
| 使用说明 | 信任等级一般，只需验证网站的真实性便可颁发证书保护网站，拥有域名的解析权即可。 | 信任等级强，须要验证企业的身份，审核严格，安全性更高。 | 信任等级最高，一般用于银行证券等金融机构，审核严格，安全性最高，同时可以激活绿色网址栏。 |
| 证书用途 | 个人 | 企业 | 金融行业 |
| 签发时间 | 数小时 | 5 个工作日 | 7 个工作日 |
| 浏览器行为 |  ![](../../_images/11.png) | ![](../../_images/11.png) | ![](../../_images/31.png)


## 共享证书 {#share}

已创建的证书除可用于当前账户下的证书绑定业务，也可共享给当前账户的子账户或者其他账户，用于其名下相应资源的证书绑定业务，具体操作方法如下：  


**第一步：共享证书**  

右键点击指定证书可以看到 “共享证书” 按钮，或者选中证书后再通过上方 “更多操作” 下的 “共享证书” 按钮  

![](../../_images/share_ssl_menu.png)

在弹出的账户选择页面，选中指定账户，可以是当前账户下的子账户，也可以为指定账户(支持 id 和邮箱两种检索方式)  

![](../../_images/share_ssl_select_user.png)


**第二步：使用共享证书**  

以被共享证书的账户登录控制台，访问控制台左侧的 安全 ->  SSL证书服务，切换上方标签至 “共享证书” 页面，可以看到共享的证书  

![](../../_images/share_ssl_list.png)

访问控制台左侧的 网络 -> 负载均衡器，切换上方标签至 “服务器证书 ”页面，可以看到共享的证书，其所有权为 “共享”   

![](../../_images/share_ssl_list_lb.png)

创建或者选择某一负载均衡器，在其 HTTPS 监听器的编辑窗口中，选择 “添加服务器证书”，弹出选择证书的窗口，可以看到共享的证书，其所有权为 “共享”  

![](../../_images/share_ssl_listener.png)


**撤销证书共享**  

以证书拥有者的账户登录控制台，访问控制台左侧的 安全 ->  SSL证书服务，点击指定证书最后一列的 “查看共享成员” 链接，在弹出窗口中，撤销指定账户的证书共享  

![](../../_images/share_ssl_cancel.png)


**注意：**  

* 某一证书被共享给用户 A，用户 A 无权共享此证书给其他账户  
* 已被共享的证书，在未撤销共享之前，无法被删除  

## FAQ {#faq}

**加密算法如何选择**

相同类型算法位数越多，性能消耗越严重，但安全性越高。 ECC 算法用较低的位数即可获取与 RSA 高位数的安全性，同时性能也比较高，但是要求客户端版本较高，旧版客户端可能不支持 ECC 算法。 具体的算法选择需要结合企业实际也许需求进行权衡。

**是否支持吊销**

支持吊销,提工单即可。

**证书过期预警**

通过 QingCloud 官方平台购买的正在，如证书即将过期，平台会提前30、15、7天，通过短信及邮件给用户发送提醒，如证书为用户自行上传的，则不会有过期提醒。

**Google 不信任 Symantec 是真是假**

该报道为误读具体参看: [《谷歌宣布Chrome不再信任所有赛门铁克SSL证书》误读新闻的澄清说明](https://www.trustasia.com/to-clarify-news-of-symantec-certificate)

**HTTPS 的性能损耗有多少**

这个取决于多方面因素，具体以实测为准，可以使用该工具测试： [HTTPS VS HTTP 测速](https://www.httpvshttps.cn/)

**如何检测证书的兼容性**

可选择使用测试工具进行测试，如 [https://myssl.com/](https://myssl.com/)

**如何选择一个合适的证书**

*   个人选择 DV 证书
*   企业选择 OV 或者 EV 证书
*   金融相关行业选择 EV 证书

以上建议仅供参考
