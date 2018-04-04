---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 关于逆向 DNS

逆向 DNS 是用于将 IP 地址解析为域名的方法，就像域名系统 (DNS) 将域名解析为关联的 IP 地址一样。逆向 DNS 的一种应用是作为垃圾邮件过滤器。通常，垃圾邮件制造者使用的是无效 IP 地址，即与域名不匹配的 IP 地址。逆向 DNS 查找程序会将传入邮件的 IP 地址输入到 DNS 数据库。如果找不到与 IP 地址匹配的有效名称，那么服务器会阻止该邮件。逆向 DNS 还用于像网络故障诊断调用（例如，`ping`）这样的操作以及用于网络监视工具。
