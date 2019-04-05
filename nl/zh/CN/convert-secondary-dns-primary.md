---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 将辅助 DNS 区域转换为主区域
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

您可以随时将[辅助 DNS 区域](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window}转换为主区域。将辅助 DNS 区域转换为主 DNS 区域时，{{site.data.keyword.BluSoftlayer_notm}} 名称服务器会成为已转换区域的权威名称服务器。执行以下步骤将辅助 DNS 区域转换为主 DNS 区域：

* 通过从导航菜单中选择**经典基础架构**，以导航至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**辅助 DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 辅助区域**。
* 从所需辅助区域的**操作**下拉列表中，选择**转换为主区域**。
* 选择**是**按钮以转换区域，或者选择**否**以取消该操作。

## 后续操作
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

将辅助 DNS 区域转换为主 DNS 区域后，可以在**转发区域**屏幕上查看该区域。先前该区域存在的所有 SOA 和 NS 记录都将替换为 {{site.data.keyword.BluSoftlayer_notm}} SOA 和 NS 记录，且无法对这些记录进行编辑。您仍可以[编辑其余区域记录](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)。
