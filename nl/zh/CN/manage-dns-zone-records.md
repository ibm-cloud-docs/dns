---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone Record, Update DNS Zone Record, edit dns zone record, add dns zone record, delete dns zone record 

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

# 管理 DNS 区域记录
{: #manage-dns-zone-records}
此部分详细描述了如何添加、编辑和删除 DNS 区域记录。

## 添加 DNS 区域记录
{: #add-a-dns-zone-record}

在[添加 DNS 区域](/docs/infrastructure/dns?topic=dns-manage-dns-zones#add-a-dns-zone)后，可以随时向该区域添加记录。这些记录包括：

* A（主机）记录
* AAAA（主机）记录
* CNAME（别名）记录
* MX（邮件交换）记录
* TXT（文本）记录
* SRV（服务）记录

执行以下步骤来添加 DNS 区域记录：

* 导航至 **DNS 区域**屏幕。请参阅[使用“DNS 区域”屏幕](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)。
* 选择要向其添加记录的 DNS 区域。
* 从**资源类型**下拉列表中，选择所需的**资源类型**。
* 填写新记录的其余字段。请参阅下表以了解更多信息：<br/><br/><table border="1"><tbody><tr><th scope="col">记录类型</th><th scope="col">字段</th><th scope="col">条目</th></tr><tr><td rowspan="3">A（主机）、AAAA（主机）或 CNAME（别名）</td><td>主机</td><td>输入<strong>主机名</strong>。</td></tr><tr><td>指向</td><td>输入主机记录指向的 <strong>IP 地址</strong>。</td></tr><tr><td>TTL</td><td>从下拉列表中选择生存时间 (TTL)。TTL 缺省值为 15 分钟。</td></tr><tr><td rowspan="4">MX（邮件交换）</td><td>优先级</td><td>输入目标主机的<strong>优先级</strong>。数字越小，优先级越高。</td></tr><tr><td>主机</td><td>输入<strong>主机名</strong>。</td></tr><tr><td>转至</td><td>输入邮件服务器的 <strong>CNAME</strong>。这通常表示为 `mail.example.com`。</td></tr><tr><td>TTL</td><td>从下拉列表中选择生存时间 (TTL)。TTL 缺省值为 15 分钟。</td></tr><tr><td rowspan="3">TXT（文本）</td><td>名称</td><td>输入 <strong>@</strong> 或<strong>域名</strong>。</td></tr><tr><td>值</td><td>输入<strong>记录</strong>以验证域或 IP 的相应电子邮件结束权。</td></tr><tr><td>TTL</td><td>从下拉列表中选择生存时间 (TTL)。TTL 缺省值为 15 分钟。</td></tr><tr><td rowspan="8">SRV（服务记录）</td><td>服务</td><td>输入所需服务的<strong>符号名称</strong>。</td></tr><tr><td>协议</td><td>从下拉列表中选择正在使用的<strong>协议</strong>。</td></tr><tr><td>优先级</td><td>输入目标主机的<strong>优先级</strong>。数字越小，优先级越高。</td></tr><tr><td>权重</td><td>对于优先级相同的记录，输入<strong>相对权重</strong>。</td></tr><tr><td>端口</td><td>输入可在其上找到服务的 <strong>TCP 或 UDP 端口</strong>。</td></tr><tr><td>主机（可选）</td><td>输入服务的<strong>主机名</strong>。</td></tr><tr><td>目标</td><td>输入提供服务的机器的<strong>规范主机名</strong>。</td></tr><tr><td>TTL</td><td>从下拉列表中选择生存时间 (TTL)。TTL 缺省值为 15 分钟。</td></tr></tbody></table><br/>
* 选择**添加记录**按钮以添加新的区域记录。

### 后续操作
{:#add-a-dns-zone-record-next}

添加区域记录后，该记录会显示在屏幕的**现有记录**部分中。您可以随时[编辑](#edit-a-dns-zone-record)或[删除](#delete-a-dns-zone-record)该区域记录。

## 编辑 DNS 区域记录
{: #edit-a-dns-zone-record}

现有 DNS 区域记录可由用户进行编辑以更新各个区域，例如生存时间 (TTL)、指针 (PTR) 记录和主机名。多个主机和别名可以随时与一个 DNS 区域记录相关联。执行以下步骤来编辑现有 DNS 区域记录。

* 通过从导航菜单中选择**经典基础架构**，以导航至所需的 **DNS 区域**屏幕。 
* 从经典基础架构导航菜单中，选择**网络 > DNS > 转发区域**。
* 单击包含任何现有记录的**行**。 

  显示为斜体的记录不可编辑。这些记录通常限于 NS（名称服务器）记录。
  {: note}
  
* 根据需要更新记录的详细信息。
* 选择**更新**按钮以更新记录，或者选择**取消**以取消该操作。

### 后续操作
{: #edit-a-dns-zone-record-next}

更新记录后，其详细信息将自动显示新条目。可以随时更新记录，还可以删除现有记录和[添加](#add-a-dns-zone-record)新的记录。

## 删除 DNS 区域记录
{: #delete-a-dns-zone-record}

删除 DNS 区域记录是通过 **DNS 编辑区域**屏幕完成的。删除 DNS 区域记录无法撤销。
* 通过单击 DNS 区域列表中的名称，选择具有要删除的记录的 DNS 区域。
* 选择包含所需记录的行末尾的“删除”图标。这将显示一个弹出确认框。
* 选择**是**按钮以确认删除，或者选择**否**按钮以取消该操作。
