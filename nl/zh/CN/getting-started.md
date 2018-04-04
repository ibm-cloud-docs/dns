---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS 入门

因特网的域名系统 (DNS) 用于将服务器和路由器识别到的 IP 地址转换为名为_域名_的给定用户友好型名称（例如 `ibm.com`）。

虽然 DNS 的概念很简单，但如果没有便利的方法，管理和存储各种域的记录可能会变得十分繁琐。

IBM Cloud DNS 为客户提供了一个集中位置，在其中可使用基本 DNS 管理界面来查看和管理自己的域。它还为用户提供了一个选项，用于在同一位置免费管理逆向和辅助 DNS。

IBM Cloud 还提供了一套额外的[网络工具](https://console.bluemix.net/docs/infrastructure/network-tools/getting-started.html#getting-started-with-network-tools)。有关通过[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 使用 DNS 界面的具体指示信息，请参阅[此文档](https://github.ibm.com/Bluemix-Docs/dns/blob/staging/using-the-dns-interface.html)。

## 工作方式
在基本级别，{{site.data.keyword.BluSoftlayer_notm}} DNS 的工作方式类似于您将使用的任何 DNS 管理工具。您可以与现有 DNS 记录交互并对其进行编辑，添加新记录，以及更新有关逆向 DNS 的信息。通过其他 DNS 管理服务来使用 {{site.data.keyword.BluSoftlayer_notm}} 或者您自己对其进行管理的主要优点是，您有一个可存储所有数据的集中、可靠的位置。

作为额外的服务，{{site.data.keyword.BluSoftlayer_notm}} 向客户免费提供辅助 DNS 区域，支持用户在发生数据丢失或节点故障时备份其主 DNS 记录。

## 如何管理 DNS
大多数用户使用[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 来管理其主 DNS、逆向 DNS 和辅助 DNS。该门户网站是即指即点界面，用于管理所有 DNS 相关操作。

您还可以选择使用 IBM Cloud SoftLayer API (SLAPI) 进行 DNS 交互。该 API 的功能与门户网站 UI 的功能几乎完全相同。但是，如果是批量编辑 DNS 记录，那么客户门户网站一批最多处理 20 个记录，而 API 的灵活性更大。有关使用 SLAPI 与 DNS 进行交互的更多信息，请参阅[此 API 文档](dns-api.html)。


