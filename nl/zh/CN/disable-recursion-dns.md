---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Disable Recursion, DNS IBM Cloud DNS servers, BIND configuration file

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 禁用 DNS 递归
{:#disable-recursion-for-dns}

缺省情况下，IBM Cloud DNS 服务器会执行递归。通过递归，DNS 服务器在自己无法解析域时可以联系其他 DNS 服务器来帮助解析域名。事实证明在必要时，递归是一种非常有用的工具；不过，递归也会导致 DNS 服务器易受攻击，可能造成 DNS 服务器完全停止运行。系统管理员通常会确定是否需要递归，然后相应进行操作。否则，最好禁用递归。根据您的操作系统或控制面板，执行以下步骤来禁用 DNS 递归。

## 在 Plesk 中禁用递归
{:#disable-recursion-in-plesk}
* 登录到 **Plesk 管理面板**。
* 选择**工具和设置**。
* 单击该部分中的 **DNS 模板设置**。
* 从 **DNS 递归**部分中，选择 **Localnets**。
* 单击**确定**按钮。

## 在 Windows Server 2003 和 2008 中禁用递归
{:#disable-recursion-in-windows-server}

* 从**开始**菜单使用 **DNS 管理器**：
  * 单击**开始**按钮。
  * 选择**管理工具**。
  * 选择 **DNS**。
* 在**控制台树**中，右键单击所需的 **DNS 服务器**。
* 选择**属性**选项卡。
* 单击**服务器选项**部分中的**高级**按钮。
* 选中**禁用递归**复选框。
* 单击**确定**按钮。

## 在 Linux 中禁用递归
{:#disable-recursion-in-linux}

 * 在操作系统中找到 BIND 配置文件。BIND 配置文件通常位于以下其中一个路径中：
  * /etc/bind/named.conf
  * /etc/named.conf
* 在首选编辑器中打开 named.conf 文件。
* 将以下详细信息添加到**选项**部分：<br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* 重新启动设备。
