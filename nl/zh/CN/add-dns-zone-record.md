---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone Record, TTL Select, Relative Weight

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 添加 DNS 区域记录
{:#add-a-dns-zone-record}

在[添加 DNS 区域](/docs/infrastructure/dns?topic=dns-add-a-dns-zone)后，可以随时向该区域添加记录。这些记录包括：

* A（主机）记录
* AAAA（主机）记录
* CNAME（别名）记录
* MX（邮件交换）记录
* TXT（文本）记录
* SRV（服务）记录

执行以下步骤来添加 DNS 区域记录：

* 导航至所需的 **DNS 区域**屏幕。请参阅[使用“DNS 区域”屏幕](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)。
* 选择要向其添加记录的 DNS 区域。
* 从**资源类型**下拉列表中，选择所需的**资源类型**。
* 填写新记录的其余字段。请参阅下表以了解更多信息：<br/><br/><table border="1"><tbody><tr><th scope="col">记录类型</th><th scope="col">字段</th><th scope="col">条目</th></tr><tr><td rowspan="3">A（主机）、AAAA（主机）或 CNAME（别名）</td><td>主机</td><td>输入<strong>主机名</strong>。</td></tr><tr><td>指向</td><td>输入主机记录指向的 <strong>IP 地址</strong>。</td></tr><tr><td>TTL</td><td>从下拉列表中选择生存时间 (TTL)。TTL 缺省值为 15 分钟。</td></tr><tr><td rowspan="4">MX（邮件交换）</td><td>优先级</td><td>输入目标主机的<strong>优先级</strong>。数字越小，优先级越高。</td></tr><tr><td>主机</td><td>输入<strong>主机名</strong>。</td></tr><tr><td>转至</td><td>输入邮件服务器的 <strong>CNAME</strong>。这通常表示为 mail.example.com。</td></tr><tr><td>TTL</td><td>从下拉列表中选择生存时间 (TTL)。TTL 缺省值为 15 分钟。</td></tr><tr><td rowspan="3">TXT（文本）</td><td>名称</td><td>输入 <strong>@</strong> 或<strong>域名</strong>。</td></tr><tr><td>值</td><td>输入<strong>记录</strong>以验证域或 IP 的相应电子邮件结束权。</td></tr><tr><td>TTL</td><td>从下拉列表中选择生存时间 (TTL)。TTL 缺省值为 15 分钟。</td></tr><tr><td rowspan="8">SRV（服务记录）</td><td>服务</td><td>输入所需服务的<strong>符号名称</strong>。</td></tr><tr><td>协议</td><td>从下拉列表中选择正在使用的<strong>协议</strong>。</td></tr><tr><td>优先级</td><td>输入目标主机的<strong>优先级</strong>。数字越小，优先级越高。</td></tr><tr><td>权重</td><td>对于优先级相同的记录，输入<strong>相对权重</strong>。</td></tr><tr><td>端口</td><td>输入可在其上找到服务的 <strong>TCP 或 UDP 端口</strong>。</td></tr><tr><td>主机（可选）</td><td>输入服务的<strong>主机名</strong>。</td></tr><tr><td>目标</td><td>输入提供服务的机器的<strong>规范主机名</strong>。</td></tr><tr><td>TTL</td><td>从下拉列表中选择生存时间 (TTL)。TTL 缺省值为 15 分钟。</td></tr></tbody></table><br/>
* 选择**添加记录**按钮以添加新的区域记录。

## 后续操作
{:#add-a-dns-zone-record-next}

添加区域记录后，该记录会显示在屏幕的**现有记录**部分中。您可以随时[编辑](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)或[删除](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone)该区域记录。
