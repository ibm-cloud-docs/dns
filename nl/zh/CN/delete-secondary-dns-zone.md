---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 删除辅助 DNS 区域
{:#delete-a-secondary-dns-zone}

创建辅助 DNS 区域后，可随时将其删除。请注意，辅助 DNS 区域一旦删除便无法恢复。执行以下步骤来删除辅助 DNS 记录。

 * 通过从导航菜单中选择**经典基础架构**，以导航至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**辅助 DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 辅助区域**。
* 从需要删除的区域的**操作**下拉列表中，选择**删除**。这将显示一个弹出确认框。如果存在多个辅助区域，那么可以对该视图进行过滤以找到要删除的区域。
  {:note}
* 选择**是**按钮以确认删除，或者选择**否**按钮以取消该操作。

## 后续操作
{:#delete-a-secondary-dns-zone-next}

删除辅助 DNS 区域后，从主区域到该辅助区域的自动传输会停止，并且该辅助区域不再存在。如果任何时候主区域需要辅助 DNS 区域，可以[创建新的辅助 DNS 区域](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone)。
