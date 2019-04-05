---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Master Nameserver

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 编辑辅助 DNS 区域
{:#edit-a-secondary-dns-zone}

可随时编辑辅助 DNS 区域以更新“主名称服务器”或“传输时间间隔”。执行以下步骤来编辑辅助 DNS 区域。

* 通过从导航菜单中选择**经典基础架构**，以导航至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中的**辅助 DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 辅助区域**。
* 单击**包含辅助 DNS 区域的行**上的任意位置以打开区域进行编辑。如果存在多个辅助区域，那么可以对该视图进行过滤以找到需要编辑的区域。
  {:note}  
* 根据需要，更新**主名称服务器**和**传输时间间隔**字段。
* 选择**更新**按钮以更新辅助 DNS 区域，或者选择**取消**以取消该操作。

## 后续操作
{:#edit-a-secondary-dns-zone-next}

编辑辅助 DNS 区域后，**主名称服务器**和**传输时间间隔**值会反映出更新，并且辅助区域将根据新信息开始接收传输。可以通过重复上面的步骤随时再次编辑区域。
