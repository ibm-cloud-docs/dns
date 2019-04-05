---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone, DNS management, Add DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 添加 DNS 区域
{:#add-a-dns-zone}

通过 {{site.data.keyword.BluSoftlayer_notm}} 进行的 DNS 管理范围可扩展到可能不在 {{site.data.keyword.BluSoftlayer_notm}} 网络上的 DNS 区域。使用我们的界面，可随时以单个域的方式或批量方式添加 DNS 区域。目前，添加 DNS 区域在[控制](https://control.softlayer.com/)版本的客户门户网站中执行。请执行以下步骤来添加一个或多个 DNS 区域

* 使用您的唯一凭证登录到[控制](https://control.softlayer.com/)版本的客户门户网站。
* 从导航菜单中，选择**经典基础架构**
* 从**网络**下拉菜单中，选择 **DNS**。
* 选择**转发区域**。
* 选择右上角的**添加 DNS 区域**选项卡。
* 确定是要添加单个域还是多个域：<br> <br><table border="1"><tbody><tr><th>如果要添加...</th><th>请执行以下步骤...</th></tr><tr><td>单个域</td><td>在屏幕的<strong>添加单个域</strong>部分中，完成以下步骤：<br> <ul><li>在<strong>域名</strong>字段中，输入<strong>域名</strong>。</li><li>在 <strong>IP 地址</strong>字段中，输入域名将指向的 <strong>IP 地址</strong>。</li><li>单击<strong>添加区域</strong>按钮以添加域。<br> </li></ul></td></tr><tr><td>多个域</td><td>确定这些域是将与单个 IP 地址还是多个 IP 相关联：<br> <p> </p><p> </p><p> </p><p> </p><ul><li>如果域将与单个 IP 地址相关联，<ul><li>在<strong>域</strong>文本框中，输入<strong>每个域</strong>。</li><li>在<strong>缺省 IP 地址</strong>字段中，输入 <strong>IP 地址</strong>。</li><li>单击<strong>添加区域</strong>按钮以批量添加域。</li></ul></li><li>如果域将与多个 IP 地址相关联，<ul><li>在<strong>域</strong>文本框中，输入<strong>每个域</strong>及其相应的 <strong>IP 地址</strong>，每个域及其 IP 地址一行。</li><li>单击<strong>添加区域</strong>按钮以批量添加域。</li></ul></li><li> </li></ul></td></tr></tbody></table>

## 后续操作
{:#add-a-dns-zone-next}

添加 DNS 区域后，该区域会显示在[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中 [DNS 区域](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)屏幕上的 DNS 区域列表中。可以随时[编辑](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)或[删除](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone)该区域。


