---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 在 cPanel/WHM 中创建专用名称服务器

使用 cPanel/WHM 产品，可以随时创建专用名称服务器。专用名称服务器允许与 Web 站点（例如，`www.yourdomain.com`）关联的名称服务器显示该 Web 站点的名称服务器（例如，`ns1.yourdomain.com`），而不是显示与该 Web 站点的 Web 主机关联的名称服务器（例如，`ns1.webhostdomain.com`）。将专用名称服务器添加到域中还会在 cPanel/WHM 中出现用于 DNS 管理的其他选项。执行本文中的步骤来创建专用名称服务器。如果在执行本过程期间或之后出现问题，请[开具凭单](/general/create-ticket.html)。

## 对名称服务器命名

* 通过以下 URL 登录到服务器上的 WHM：http://xx.xx.xx.xx:2086。
* 从**服务器配置**菜单中，选择**基本 cPanel/WHM 设置**。
* 在以下一个或多个字段中，输入所需的名称服务器主机名：
  * 主名称服务器
  * 辅助名称服务器
  * 第三名称服务器
  * 第四名称服务器
* 选择**保存**按钮。

## 为域创建区域文件

* 从 **DNS 功能**菜单中，选择**添加 DNS 区域**。
* 在 **IP** 字段中，输入域的 **IP 地址**。
* 在**区域**字段中，输入**域名**。

**注：**或者，也可以使用 cPanel 的 WHM 文档中的[创建帐户](http://docs.cpanel.net/twiki/bin/view/AllDocumentation/WHMDocs/CreateAccount)指南来创建域帐户。

## 向名称服务器分配 IP

* 从**网络设置**菜单中，选择**名称服务器 IP**。
* 在**名称服务器**字段中，输入第一个**名称服务器名称**。
* 选择**分配**按钮。
* 对每个名称服务器重复上述步骤。

## 设置名称服务器

* 从**服务配置**菜单中，选择**名称服务器设置**。
* 选择弹出消息上的**继续**按钮。
