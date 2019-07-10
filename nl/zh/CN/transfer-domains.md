---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-15"

keywords: Transfer Existing Domain, Transfer multiple domains 

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 传输域
{: #transfer-domains}

## 将现有域传输到 IBM Cloud
{:#transfer-an-existing-domain-to-ibm-cloud}

一旦注册域后，就可以随时传输该域。通过将域从第三方注册器传输到 {{site.data.keyword.cloud}}，可以简化域管理过程。传输域不会影响 Web 站点、电子邮件或 DNS。它仅更改用于管理域记录的注册器。执行本文中的步骤将现有域传输到 {{site.data.keyword.cloud_notm}}。

## 传输单个域
{: #transfer-single-domain}

* 导航至 [{{site.data.keyword.cloud_notm}} 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**域注册**屏幕。请参阅[访问“域注册”屏幕](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen)。
* 选择**传输**选项卡。
* 在**域名**字段中，输入现有域名。
* 从**域类型**下拉列表中，选择域类型。
* 从**注册时间**下拉列表中，选择域将保持活动的时间长度。

  每个时间段的价格会显示在该时间长度旁边，在更新域时，将按该价格对信用卡收费或从帐户中扣除信用值。
{:note}
  
* 选择**继续**按钮以传输域。

## 传输多个域
{: #transfer-multiple-domains}

如果帐户上有一张有效信用卡或者有可用信用值，那么可以随时将域批量传输到 {{site.data.keyword.cloud_notm}}，而不用逐个进行传输。执行以下步骤来为 {{site.data.keyword.cloud_notm}} 传输多个域。

* 导航至 [{{site.data.keyword.cloud_notm}} 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**域注册**屏幕。请参阅[访问“域注册”屏幕](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen)。
* 选择**传输**选项卡。
* 选择**传输**选项卡中的**传输多个域？**选项。
* 在**域名**字段中，输入现有域名。
* 从**域类型**下拉列表中，选择域类型。
* 从**注册时间**下拉列表中，选择域传输后将保持活动的时间长度。

每个时间段的价格会显示在该时间长度旁边，在更新域时，将按该价格对信用卡收费或从帐户中扣除信用值。
{:note}

* 对要传输的其他每个域进行重复操作。

选择**添加另一个项**选项可填充其他空白字段以获得更多域条目。选择**删除**图标可从屏幕中删除整个条目。
{:note}

* 选择**继续**按钮以传输域。



## 后续操作
{:#transfer-an-existing-domain-to-ibm-cloud-next}

传输域后，可以在[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 中对其进行管理。域的注册接近其到期日期时，可通过**域管理**屏幕对其进行[更新](/docs/infrastructure/dns?topic=dns-renew-an-existing-domain)。
