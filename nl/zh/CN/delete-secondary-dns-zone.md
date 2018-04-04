---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 删除辅助 DNS 区域

创建辅助 DNS 区域后，可随时将其删除。请注意，如果删除了辅助 DNS 区域，无法取回该区域。执行以下步骤来删除辅助 DNS 记录。

 * 浏览至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 中的**辅助 DNS 区域**屏幕。请参阅[使用“DNS 区域”屏幕](use-dns-zones-screen.html){:new_window}。
* 从需要删除的区域的**操作**下拉列表中，选择**删除**。这将显示一个弹出确认框。**注：**如果存在多个辅助区域，那么可以对该视图进行过滤以找到要删除的区域。
* 选择**是**按钮以确认删除，或者选择**否**按钮以取消该操作。

## 后续操作

删除辅助 DNS 区域后，从主区域到该辅助区域的自动传输会停止，并且该辅助区域不再存在。如果任何时候主区域需要辅助 DNS 区域，可以[创建新的辅助 DNS 区域](add-secondary-dns-zone.html)。
