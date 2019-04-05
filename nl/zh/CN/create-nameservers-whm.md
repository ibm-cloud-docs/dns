---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: create your own nameservers, cPanel, WHM

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 在 cPanel/WHM 中创建自己的名称服务器
{:#create-your-own-nameservers-in-cpanel-whm}

本文提供了有关如何使用 Web 主机管理器 (WHM) 来创建自己的名称服务器的步骤。如果在执行这些步骤后遇到问题，请参阅本文来提交支持凭单。

1. 首先，确定名称服务器的名称。例如，假设托管公司名为“Awesome Server Hosting”，因此您希望设置 `ns1.awesomeserverhosting.com` 和 `ns2.awesomeserverhosting.com`。

* 通过在浏览器中转至 `https://XX.XX.XX.XX:2087` 来登录到服务器上的 WHM。

* 要设置名称服务器，请选择左侧栏中的第一个选项，该选项应该为“基本 cPanel/WHM 设置”。 

 * 在此可以设置主名称服务器、辅助名称服务器、第三名称服务器和第四名称服务器的名称。

 * 完成后，选择“保存”按钮。

2. 现在，在您的服务器中为 `awesomeserverhosting.com` 创建区域文件。有两种方法可以执行此任务：

第一种方法：为“awesomeserverhosting.com”创建域帐户。有关此问题的指示信息不在本文讨论范围内，请参阅 [cPanel 文档](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)以获取更多信息： 

   * 在左侧边栏中的“DNS 功能”下，选择“添加 DNS 区域”。

   * 为 `awesomeserverhosting.com` 提供托管主 Web 站点的 IP 地址，当然，还请提供域名。

   **注：仅当您不打算在此服务器上托管 `awesomeserverhosting.com` 时才执行此操作！**

   * 在**联网设置**标题下，单击**名称服务器 IP**。

   * 提供名称服务器的名称。例如，提交 `ns1.awesomeserverhosting.com`，然后提交 `ns2.awesomeserverhosting.com`。

   * 在左侧栏中，找到**服务配置**下的**名称服务器设置**。

   * 这将显示类似以下内容的消息：“我们建议您不要启用不打算使用的名称服务器。如果您希望禁用名称服务器，那么始终可以在服务管理器中将其禁用。”

   * 在此我们使名称服务器启动并运行，所以请选择标记为**继续 >>** 的按钮。`cPanel` 工具会确保您已将正确的包安装到服务器上，并确保这些包配置为正确运行以托管您的域名服务。现在您已一切准备就绪！

外部链接：

* [cPanel 文档](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
