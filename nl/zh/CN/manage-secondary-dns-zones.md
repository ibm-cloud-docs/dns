---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# 管理辅助 DNS 区域
{: #manage-secondary-dns-zones}

{{site.data.keyword.cloud}} 为所有客户提供了辅助 DNS，用于在发生数据丢失时对主 DNS 区域进行高速缓存。维护辅助 DNS 区域不是必需的，但对于具有多个域的用户，强烈建议这样做。 


## 添加辅助 DNS 区域
{:#add-a-secondary-dns-zone}

执行以下步骤来添加辅助 DNS 区域：

* 通过从导航菜单中选择**经典基础架构**，以导航至 [{{site.data.keyword.cloud_notm}} 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**辅助 DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 辅助区域**。
* 选择**添加区域**选项卡。
* 在**区域**字段中，输入**区域的域**。
* 在**主名称服务器**字段中，输入**主名称服务器的 IP 地址**。
* 在**传输时间间隔**字段中，输入主 DNS 区域传输到辅助 DNS 区域的**传输时间**（以分钟为单位）。
* 选择**添加**按钮以添加区域，或者选择**取消**以取消该操作。

### 添加之后执行的操作
{:#add-a-secondary-dns-zone-next}

创建辅助 DNS 区域后，该区域会显示在“辅助 DNS 区域”屏幕上的区域列表中。将数据从主区域传输到辅助区域会按您在创建区域时指定的时间间隔执行。您可以随时[编辑](#edit-a-secondary-dns-zone)、[手动传输](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone)该区域或将其[转换](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone)为主区域。还可以随时[删除](#delete-a-secondary-dns-zone)辅助 DNS 区域。

## 编辑辅助 DNS 区域
{:#edit-a-secondary-dns-zone}

可随时编辑辅助 DNS 区域以更新“主名称服务器”或“传输时间间隔”。执行以下步骤来编辑辅助 DNS 区域。

* 通过从导航菜单中选择**经典基础架构**，以导航至 [{{site.data.keyword.cloud_notm}} 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**辅助 DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 辅助区域**。
* 单击**包含辅助 DNS 区域的行**上的任意位置以打开区域进行编辑。如果存在多个辅助区域，那么可以对该视图进行过滤以找到需要编辑的区域。
  {:note}  
* 根据需要，更新**主名称服务器**和**传输时间间隔**字段。
* 选择**更新**按钮以更新辅助 DNS 区域，或者选择**取消**以取消该操作。

### 编辑之后执行的操作
{:#edit-a-secondary-dns-zone-next}

编辑辅助 DNS 区域后，**主名称服务器**和**传输时间间隔**值会反映出更新，并且辅助区域将根据新信息开始接收传输。可以通过重复先前步骤随时再次编辑区域。

## 删除辅助 DNS 区域
{:#delete-a-secondary-dns-zone}

创建辅助 DNS 区域后，可随时将其删除。请注意，辅助 DNS 区域一旦删除便无法恢复。执行以下步骤来删除辅助 DNS 记录。

 * 通过从导航菜单中选择**经典基础架构**，以导航至 [{{site.data.keyword.cloud_notm}} 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**辅助 DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 辅助区域**。
* 从需要删除的区域的**操作**下拉列表中，选择**删除**。这将显示一个弹出确认框。如果存在多个辅助区域，那么可以对该视图进行过滤以找到要删除的区域。
  {:note}
* 选择**是**按钮以确认删除，或者选择**否**按钮以取消该操作。

### 删除之后执行的操作
{:#delete-a-secondary-dns-zone-next}

删除辅助 DNS 区域后，从主区域到该辅助区域的自动传输会停止，并且该辅助区域不再存在。如果任何时候主区域需要辅助 DNS 区域，可以[创建新的辅助 DNS 区域](#add-a-secondary-dns-zone)。
