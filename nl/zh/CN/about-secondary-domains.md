---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 关于辅助域

辅助域是 {{site.data.keyword.BluSoftlayer_notm}} DNS 服务器从您的服务器传输到我们的权威 DNS 服务器（`ns1.softlayer.com` 和 `ns2.softlayer.com`）的域。您可以在门户网站中，通过单击**<span style="text-decoration: underline">公用网络</span>**文件夹中的**<span style="text-decoration: underline">域名系统</span>**，单击**<span style="text-decoration: underline">辅助 DNS</span>** 链接，最后单击**<span style="text-decoration: underline">添加辅助 DNS 记录</span>**来配置辅助域。

要设置辅助域，您需要三条信息：域、要从该域传输的*主 DNS 服务器的 IP 地址*以及您希望传输域的频率（以分钟为单位）。<br/>
配置辅助域后，您将能够更改主服务器的 IP 地址和传输时间间隔。您还可以在传输时查看域，也可以请求手动传输域，将辅助域转换为主域，以及查看在传输过程中记录的任何错误消息。
