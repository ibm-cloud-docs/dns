---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-13"

keywords: DNS servers, fast domain name resolution, DNS FAQ

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}


# DNS 常見問題
{:#dns-faq}

## 何謂 DNS 伺服器？
{:#what-are-dns-servers}
{: faq}

161.26.0.10 及 161.26.0.11

## 何謂本端 DNS 解析器？
{:#what-are-local-dns-resolvers}
{: faq}

在我們專用網路上的本端解析名稱伺服器為：

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

這些名稱伺服器提供的快速網域名稱解析不會耗盡公用頻寬配額。如果要使用它們，請遵循正確的程序，將解析名稱伺服器新增至作業系統。

## {{site.data.keyword.BluSoftlayer_notm}} 名稱伺服器位址為何？
{:#what-are-name-server-addresses}
{: faq}

我們有兩個位址給「主名稱伺服器」，以及兩個位址給「解析名稱伺服器」。

### 主名稱伺服器
{:#authoratative-name-servers}

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### 解析名稱伺服器
{:#resolving-name-servers}

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

這些本端解析名稱伺服器位於專用網路上，因此它們不會耗盡公用頻寬配額。 

## 哪些 IBM Cloud DNS 伺服器會回應次要網域？
{:#what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}

{{site.data.keyword.BluSoftlayer_notm}} Anycast、已啟用 IPv 的主 DNS 伺服器將回應您的次要網域。可在下列位址找到這些伺服器：

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## 哪些 IP 位址將用於次要網域區域傳送？
{:#which-ipaddresses-secondary-domain-zone-transfers}
{: faq}

次要網域的傳送將來自下列四個 IP 位址之一：

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## 公用與專用名稱伺服器之間的差異為何？
{:#public-v-private-nameservers}
{: faq}

公用名稱伺服器是作為位於 DNS 伺服器中的網域名稱的主名稱伺服器，它們是透過[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 來管理。這些伺服器會針對一般網際網路移入來「回應」網域名稱，以及將網域名稱「解析」成 IP 位址。

我們的解析名稱伺服器位於專用網路上，並作為您伺服器的 DNS 解析器。專用解析器會查詢網際網路的根名稱伺服器來進行網域查閱。例如，從伺服器傳送郵件時，會要求對目的地網域名稱進行 NSlookup。專用 DNS 伺服器透過專用網路解析此資訊，以降低頻寬使用率、減少主伺服器上的負載，以及提供快速解析。專用網路解析器是我們為客戶提供的一項便利服務。

## 我的名稱伺服器選項為何？
{:#what-are-my-name-server-options-faq}
{: faq}

若使用裸機伺服器，名稱伺服器有四個一般選項：

* 使用網域名稱登記員的名稱伺服器來管理網域名稱。
* 使用 {{site.data.keyword.BluSoftlayer_notm}} 名稱伺服器來管理網域名稱。
* 使用協力廠商 DNS 服務來管理網域名稱。
* 在伺服器上執行您自己的名稱伺服器來管理網域名稱。

就前三個選項而言，您將使用協力廠商的名稱伺服器（例如，`ns1.softlayer.com` 及 `ns2.softlayer.com`）。最後一個選項使用您的網域作為名稱伺服器（例如，`ns1.yourdomain.com` & `ns2.yourdomain.com`），而且它需要您在伺服器上執行 DNS 服務。您也必須向登記員登錄您的網域作為名稱伺服器。名稱伺服器登錄通常是免費的，但除了基本網域名稱登錄程序之外，它需要一個額外步驟。

我們的客戶有免費的 DNS 服務，這些服務完全是透過[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 來管理。我們強烈建議讓 {{site.data.keyword.BluSoftlayer_notm}} 來管理您的 DNS 伺服器和名稱伺服器，因為我們有備援系統、管理方便，而且能夠快速進行 DNS 相關問題的疑難排解。

## 如何設定我的反向 DNS？
{:#how-do-i-setup-reverse-dns}
{: faq}

反向 DNS 設定是使用我們的[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 來進行。如需有關如何設定「反向 DNS」的指示，請參閱[更新反向 DNS 記錄](/docs/infrastructure/dns?topic=dns-update-reverse-dns-record)。


## 傳播 DNS 變更需要多久的時間？
{:#how-long-for-dns-changes-propagate}
{: faq}

DNS 變更傳播時間視 DNS 記錄的存活時間 (TTL) 設定而定。

預設 TTL 為一天，這表示對網域名稱所做的任何修改需要一天的時間傳播到整個網際網路。如果您打算頻繁地進行變更，則可以降低 TTL，不過，TTL 越低，名稱伺服器上的負載會越高。負載越高，可能會使得對一般使用者的回應時間增加，而影響其整體滿意度。

因為本端 ISP 快取的緣故，TTL 設定越高，DNS 效能就越高。TTL 設定越低，則會因為增加名稱解析而降低 DNS 效能。

若要驗證 TTL，請檢查網域的「授權開始 (SOA)」記錄。[CentralOps.net ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://centralops.net/co/) 提供檢閱網域資訊的理想工具。

所列出的 TTL 是以秒為單位。除以 60 是將 TTL 轉換為分鐘，或除以 3600 來轉換為小時。


## 傳送網域之後，網域及進行的變更需要多久的時間才看得見？
{:#how-long-transfer-change-visiblity}
{: faq}

在傳送完成之後，您的網域及/或其變更將立即出現在 IBM Cloud DNS 伺服器上。由於 DNS 的傳播本質，這些變更要出現在其他 DNS 伺服器之前會稍微延遲。

## 我是否可以在專用網路上完成 AXFR 要求？
{:#axfr-request-private-network}
{: faq}

目前，{{site.data.keyword.BluSoftlayer_notm}} 不支援專用網路上的 AXFR 要求。所有 AXFR 要求都必須在公用網路上完成。
