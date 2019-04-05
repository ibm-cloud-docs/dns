---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: IBM Cloud name server addresses, Authoritative Name Servers, domain names

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# 名稱伺服器常見問題
{:#nameserver-faqs}

## 何謂 IBM Cloud 名稱伺服器位址？
{:#what-are-the-ibm-cloud-name-server-addresses}

我們有兩個位址給「主名稱伺服器」，以及兩個位址給「解析名稱伺服器」。

**主名稱伺服器**

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

**解析名稱伺服器**

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12


## SoftLayer 上的公用與專用名稱伺服器之間的差異為何？
{:#what-is-the-difference-public-private-nameserver}

公用名稱伺服器是作為位於 DNS 伺服器中的網域名稱的主名稱伺服器，它們是透過「客戶入口網站」來管理。這些伺服器會針對一般網際網路移入來「回應」網域名稱，以及將網域名稱「解析」成 IP 位址。

解析名稱伺服器位於專用網路上，並作為您伺服器的 DNS 解析器。專用解析器會查詢網際網路的根名稱伺服器來進行網域查閱。例如，從伺服器傳送郵件時，會要求對目的地網域名稱進行 NSlookup。專用 DNS 伺服器透過專用網路解析此資訊，以降低頻寬使用率、減少主伺服器上的負載，以及提供快速解析。專用網路解析器是我們為客戶提供的一項便利服務。

## 我的名稱伺服器選項為何？
{:#what-are-my-name-server-options}

若使用裸機伺服器，名稱伺服器有四個一般選項：

1. 使用網域名稱登記員的名稱伺服器來管理網域名稱。
2. 使用 IBM Cloud 名稱伺服器來管理網域名稱。
3. 使用協力廠商 DNS 服務來管理網域名稱。
4. 在伺服器上執行您自己的名稱伺服器，以管理您的網域名稱。

就選項 1、2、3 而言，您將使用協力廠商的名稱伺服器（例如，`ns1.softlayer.com` 及 `ns2.softlayer.com`）。對於選項號碼 4，您將使用您的網域作為名稱伺服器 (`ns1.yourdomain.com` & `ns2.yourdomain.com`)。選項號碼 4 需要您在伺服器上執行 DNS 服務，而且您也必須向登記員登錄您的網域作為名稱伺服器。此登錄通常是免費的，但除了基本網域名稱登錄程序之外，它需要一個額外步驟。

IBM Cloud 提供免費的 DNS 服務，這些服務完全是透過[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 來管理。我們強烈建議讓 IBM Cloud 來管理您的 DNS 並作為名稱伺服器，因為我們有備援系統、管理方便，而且能夠快速進行 DNS 相關問題的疑難排解。


## 如何執行我自己的名稱伺服器？
{:#how-can-i-run-my-own-nameservers}

執行及管理您自己的名稱伺服器的最簡單方式是使用控制台工具，例如 **Plesk** 或 **cPanel**。這兩個產品都已建置在網域名稱伺服器中，可讓您新增、修改或刪除網域名稱。

若要開始，請向網域名稱登記員登錄您的網域名稱作為名稱伺服器，並指派伺服器 IP 範圍內的兩個 IP 位址。
