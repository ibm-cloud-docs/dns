---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 添加或编辑 PTR（指针）记录

PTR（即指针）记录用于将 IP 地址解析为主机名。用户可以使用[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){:new_window} 上的“逆向 DNS”功能，添加要与 IP 地址关联的 PTR 记录。另外，可以用添加 PTR 记录的方式来编辑 PTR 记录。执行以下步骤来为设备添加或编辑 PTR 记录：

1. 从**设备列表**中检索将接收 PTR 记录的设备的**公共 IP 地址**。
* 显示**逆向 DNS 记录**屏幕。请参阅[使用“DNS 区域”屏幕](use-dns-zones-screen.html)。
* 在**查看 IP** 字段中，输入从设备列表检索到的**公共 IP 地址**。
* 单击包含**逆向记录**详细信息的行上的任意位置以打开该行进行编辑。
* 根据下表填写或更新记录的字段：<br/><br/><table border="1"><tbody><tr><th>字段</th><th>条目</th></tr><tr><td>逆向 DNS</td><td>IP 地址将解析为的主机名。</td></tr><tr><td>逆向 TTL</td><td>新记录的生存时间 (TTL)</td></tr><tr><td>注释</td><td>关于记录的任何适用注释</td></tr></tbody></table><br/>
* 单击**更新**按钮以更新记录。单击**取消**以取消该操作。

## 后续操作

添加 PTR 记录后，与该记录关联的“公共 IP 地址”将解析为该记录中指定的主机名。可随时编辑该记录。要从 PTR 记录中除去详细信息，请使用**编辑**过程从字段中删除所有信息。
