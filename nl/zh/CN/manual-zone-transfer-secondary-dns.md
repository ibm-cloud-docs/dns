---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 为辅助 DNS 区域进行手动区域传输

通常，DNS 区域传输根据已指定的辅助 DNS 传输时间间隔自动完成。可以使用手动区域传输来强制传输本该等到下一次自动传输的内容。要完成手动传输，[必须建立辅助 DNS 区域](add-secondary-dns-zone.html)。执行本文中的步骤来为辅助 DNS 进行手动区域传输。

1. 浏览至[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/) 中的**辅助 DNS 区域**屏幕。请参阅[使用“DNS 区域”屏幕](delete-secondary-dns-record.html){:new_window}。
2. 从**操作**下拉列表中，选择**强制传输**以开始传输。

## 后续操作

传输开始后，“状态”将更改为**正在传输**。手动传输开始后即无法取消。传输数据后，数据传输会恢复为按先前为辅助 DNS 设置的传输时间间隔执行。[传输时间间隔可随时更改](edit-secondary-dns-zone.html)，从而无需频繁进行手动区域传输。
