---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 更新逆向 DNS 记录

通过逆向 DNS，用户能够识别与 IP 地址关联的域。客户可以随时更新其逆向 DNS 记录以更改 PTR 和生存时间 (TTL)。在**管理**版本的[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 中，可以使用**搜索和替换**工具批量更新 PTR 记录。此工具支持在“搜索”字段中输入 PTR 的一部分或完整 PTR，并使用所需信息替换对应 PTR 中的每个显示项。 

请注意，仅当现有 PTR 与服务器或 VLAN 关联时，此工具才有效。如果不存在 PTR，那么不会列出任何详细信息，并且尝试更新将生成错误。 

要添加逆向 DNS PTR 记录，请参阅[添加和编辑 PTR（指针）记录](add-and-edit-ptr-pointer-record.html)。执行以下步骤来更新逆向 DNS 记录：

 * 使用您的唯一凭证浏览至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/)。
 * 从**网络**下拉菜单中，选择 **DNS**。
 * 选择**逆向 DNS** 菜单选项。
 * 确定是必须对网络 VLAN 中的所有对应 IP 地址进行更新，还是对单个 IP 进行更改。<br><br><table border="1"><tbody><tr><th>如果更新对象是...</th><th>请执行以下步骤...</th></tr><tr><td>单个 IP</td><td><ul><li>选择<b>下拉菜单</b>以查看 IP 地址</li><li>单击所需的 <strong>IP 地址</strong>以查看与服务器关联的逆向 DNS 详细信息。</li></ul></td></tr><tr><td>网络 VLAN 上的所有对应 IP 地址</td><td><ul><li>按如上所述选择 IP 后，选择<strong>查看 IP</strong> 选项。</li><li>选择<strong>编辑此子网中所有 IP 的 RDNS</strong> 选项。</li></ul></td></tr></tbody></table><br/>
 * 对于单个 IP，只需添加**主机名**和**逆向 TTL**，然后选择**保存**即可。对于整个**子网**，请突出显示**逆向 DNS** 列下的空白处并添加**主机名**，然后选择**更新**按钮。需要对子网中的每个 IP 地址执行此任务。
