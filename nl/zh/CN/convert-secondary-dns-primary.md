---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 将辅助 DNS 区域转换为主区域

您可以随时将[辅助 DNS 区域](add-secondary-dns-zone.html){:new_window}转换为主区域。将辅助 DNS 区域转换为主 DNS 区域时，{{site.data.keyword.BluSoftlayer_notm}} 名称服务器会成为已转换区域的权威名称服务器。执行以下步骤将辅助 DNS 区域转换为主 DNS 区域：

* 浏览至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 中的**辅助 DNS 区域**屏幕。请参阅[使用“DNS 区域”屏幕](use-dns-zones-screen.html){:new_window}。
* 从所需辅助区域的**操作**下拉列表中，选择**转换为主区域**。
* 选择**是**按钮以转换区域，或者选择**否**以取消该操作。

## 后续操作

将辅助 DNS 区域转换为主 DNS 区域后，可以在**转发区域**屏幕上查看该区域。先前该区域存在的所有 SOA 和 NS 记录都将替换为 {{site.data.keyword.BluSoftlayer_notm}} SOA 和 NS 记录，且无法对这些记录进行编辑。您仍可以[编辑其余区域记录](edit-dns-zone-record.html)。
