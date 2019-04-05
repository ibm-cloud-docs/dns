---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, IBM Cloud, Add Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 添加辅助 DNS 区域
{:#add-a-secondary-dns-zone}

{{site.data.keyword.BluSoftlayer_notm}} 为所有客户提供了辅助 DNS，用于在发生数据丢失时对主 DNS 区域进行高速缓存。维护辅助 DNS 区域不是必需的，但对于具有多个域的用户，强烈建议这样做。执行以下步骤来添加辅助 DNS 区域：

* 通过从导航菜单中选择**经典基础架构**，以导航至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**辅助 DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 辅助区域**。
* 选择**添加区域**选项卡。
* 在**区域**字段中，输入**区域的域**。
* 在**主名称服务器**字段中，输入**主名称服务器的 IP 地址**。
* 在**传输时间间隔**字段中，输入主 DNS 区域传输到辅助 DNS 区域的**传输时间**（以分钟为单位）。
* 选择**添加**按钮以添加区域，或者选择**取消**以取消该操作。

## 后续操作
{:#add-a-secondary-dns-zone-next}

创建辅助 DNS 区域后，该区域会显示在“辅助 DNS 区域”屏幕上的区域列表中。将数据从主区域传输到辅助区域会按您在创建区域时指定的时间间隔执行。您可以随时[编辑](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)、[手动传输](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone)该区域或将其[转换](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone)为主区域。还可以随时[删除](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone)辅助 DNS 区域。
