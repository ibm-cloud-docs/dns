---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 管理 DNS 区域
{: #manage-dns-zones}

## 添加 DNS 区域
{: #add-a-dns-zone}

通过 {{site.data.keyword.cloud}} 进行的 DNS 管理范围可扩展到可能不在 {{site.data.keyword.cloud_notm}} 网络上的 DNS 区域。使用我们的界面，可随时以单个域的方式或批量方式添加 DNS 区域。目前，添加 DNS 区域在 [IBM Cloud 控制台](https://{DomainName}/)中执行。请执行以下步骤来添加一个或多个 DNS 区域。

* 使用您的唯一凭证登录到 [IBM Cloud 控制台](https://{DomainName}/)。
* 从导航菜单中，选择**经典基础架构**
* 从**网络**下拉菜单中，选择 **DNS**。
* 选择**转发区域**。
* 选择右上角的**添加 DNS 区域**选项卡。
* 确定是要添加单个域还是多个域：

|如果要添加...|请执行以下步骤...|
|---|---|
|单个域|在屏幕的**添加单个域**部分中，完成以下步骤：<ul><li>在**域名**字段中，输入**域名**。</li><li>在 **IP 地址**字段中，输入域名将指向的 **IP 地址**。</li><li>单击**添加区域**按钮以添加域。</li></ul>|
|多个域|确定这些域是将与单个 IP 地址还是多个 IP 相关联：<ul><li>如果域将与单个 IP 地址相关联，<ul><li>在**域**文本框中，输入**每个域**。</li><li>在**缺省 IP 地址**字段中，输入 **IP 地址**。</li><li>单击**添加区域**按钮以批量添加域。</li></ul></li><li>如果域将与多个 IP 地址相关联，<ul><li>在**域**文本框中，输入**每个域**及其相应的 **IP 地址**，每个域及其 IP 地址独占一行。</li><li>单击**添加区域**按钮以批量添加域。</li></ul></li></ul>


### 后续操作
{:#add-a-dns-zone-next}

成功添加单个区域后，将自动重定向到“区域编辑”页面。
新 DNS 区域会显示在 [IBM Cloud 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中 [DNS 区域屏幕](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)上的 DNS 区域列表中。可以随时[编辑](#edit-a-dns-zone)或[删除](#delete-a-dns-zone)该区域。

## 编辑 DNS 区域
{: edit-a-dns-zone}
通过单击区域的名称，从 DNS 区域屏幕中的区域列表中选择要编辑的 DNS 区域。这将打开“DNS 编辑区域”页面。您可以在此处更改 DNS 区域，并单击**更新 SOA** 来提交更改。 

**编辑 DNS 区域**屏幕允许您为正在编辑的区域添加新记录和编辑现有记录。您还可以从此屏幕导出或删除区域。

### 后续操作
{:#edit-a-dns-zone-next}

单击**查看所有 DNS 区域**，以返回到 DNS 区域列表。


## 删除 DNS 区域
{: #delete-a-dns-zone}

添加 DNS 区域后，可随时将其删除。DNS 区域删除是永久性操作，无法撤销。执行以下步骤来删除 DNS 区域：

* 通过从导航菜单中选择**经典基础架构**，以导航至所需的 **DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS**，然后选择所需的区域类型。
* 选择包含所需 DNS 区域的行末尾的**删除**图标。这将显示一个弹出确认框。
* 选择**是**按钮以确认删除，或者选择**否**按钮以取消该操作。

还可以从“编辑 DNS 区域”屏幕中删除区域。
{:tip}

### 后续操作
{:#delete-a-dns-zone-next}

删除 DNS 区域后，将无法再使用 [IBM Cloud 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 对该区域进行管理。要在仪表板中重新管理已删除的区域，必须将其[添加为新区域](#add-a-dns-zone)。
