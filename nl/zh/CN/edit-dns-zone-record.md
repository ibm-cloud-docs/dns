---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Update DNS Zone Record, edit dns zone record

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 编辑 DNS 区域记录
{:#edit-a-dns-zone-record}

现有 DNS 区域记录可由用户进行编辑以更新各个区域，例如生存时间 (TTL)、指针 (PTR) 记录和主机名。在任意给定时间，多个主机和别名只能与一个 DNS 区域记录相关联。执行以下步骤来编辑现有 DNS 区域记录。

* 通过从导航菜单中选择**经典基础架构**，以导航至所需的 **DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 转发区域**。
* 单击包含任何现有记录的**行**。**注：**显示为斜体的记录不可编辑。这种情况通常限于 NS（即名称服务器）记录。
* 根据需要更新记录的详细信息。
* 选择**更新**按钮以更新记录，或者选择**取消**以取消该操作。

## 后续操作
{:#edit-a-dns-zone-record-next}

更新记录后，其详细信息将自动显示新条目。可以随时更新记录，还可以删除现有记录和[添加](/docs/infrastructure/dns?topic=dns-add-a-dns-zone-record)新的记录。
