---
copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-02-26"

keywords: Reverse DNS Record, Reverse DNS, IP address, Individual IP Select

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 更新逆向 DNS 记录
{:#update-reverse-dns-record}

通过逆向 DNS，用户能够识别与 IP 地址关联的域。客户可以随时更新其逆向 DNS 记录以更改 PTR 和生存时间 (TTL)。在**管理**版本的 [IBM Cloud 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 中，可以使用**搜索和替换**工具批量更新 PTR 记录。此工具支持在“搜索”字段中输入 PTR 的一部分或完整 PTR，并使用所需信息替换对应 PTR 中的每个显示项。 

请注意，仅当现有 PTR 与服务器或 VLAN 关联时，此工具才有效。如果不存在 PTR，那么不会列出任何详细信息，并且尝试更新将生成错误。 

要添加逆向 DNS PTR 记录，请参阅[添加和编辑 PTR（指针）记录](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record)。执行以下步骤来更新逆向 DNS 记录：

 * 使用您的唯一凭证导航至 [IBM Cloud 控制台 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/)。
 * 从导航菜单中，选择**经典基础架构**。
 * 从经典基础架构导航菜单中，选择**网络 > DNS > 逆向 DNS**。
 * 输入 IP 地址，或从下拉菜单中选择该地址，然后单击**查看 IP**。
 * 编辑列出的选项，然后单击**保存**。您还可以选择**编辑此子网中所有 IP 的 RDNS** 以在整个子网中进行更改。 
 

