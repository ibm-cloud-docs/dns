---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 關於反向 DNS

反向 DNS 是將 IP 位址解析成網域名稱的方法，就像網域名稱系統 (DNS) 將網域名稱解析成相關聯的 IP 位址一樣。例如，垃圾郵件過濾器就是反向 DNS 的一種應用。通常，濫發垃圾郵件者會使用無效的 IP 位址，也就是不符合網域名稱的位址。反向 DNS 查閱程式會將送入訊息的 IP 位址輸入 DNS 資料庫中。如果找不到符合該 IP 位址的有效名稱，則伺服器會封鎖該訊息。反向 DNS 也用於諸如網路疑難排解呼叫的作業（例如 `ping`）及網路監視工具。
