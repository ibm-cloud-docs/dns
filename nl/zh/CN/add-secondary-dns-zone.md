---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 添加辅助 DNS 区域

{{site.data.keyword.BluSoftlayer_notm}} 为所有客户提供了辅助 DNS，用于在发生数据丢失时对主 DNS 区域进行高速缓存。维护辅助 DNS 区域不是必需的，但对于具有多个域的用户，强烈建议这样做。执行以下步骤来添加辅助 DNS 区域：

* 浏览至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 中的**辅助 DNS 区域**屏幕。请参阅[使用“DNS 区域”屏幕](use-dns-zones-screen.html){:new_window}。
* 选择**添加区域**选项卡。
* 在**区域**字段中，输入**区域的域**。
* 在**主名称服务器**字段中，输入**主名称服务器的 IP 地址**。
* 在**传输时间间隔**字段中，输入主 DNS 区域传输到辅助 DNS 区域的**传输时间**（以分钟为单位）。
* 选择**添加**按钮以添加区域，或者选择**取消**以取消该操作。

## 后续操作

创建辅助 DNS 区域后，该区域会显示在“辅助 DNS 区域”屏幕上的区域列表中。将数据从主区域传输到辅助区域会按您在创建区域时指定的时间间隔执行。您可以随时[编辑](edit-secondary-dns-zone.html)、[手动传输](make-manual-zone-transfer-secondary-dns.html)该区域或将其[转换](convert-secondary-dns-zone-primary-zone.html)为主区域。还可以随时[删除](delete-secondary-dns-zone.html)辅助 DNS 区域。
