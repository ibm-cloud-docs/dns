---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-03"

keywords: IBM Cloud DNS, DNS

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 開始使用 DNS 
{: #getting-started}

網際網路的「網域名稱系統 (DNS)」是一種方法，用來將伺服器和路由器所辨識的 IP 位址，轉換成對使用者友善的給定名字，稱為_網域名稱_，例如 `ibm.com`。

雖然 DNS 的概念非常簡單，但如果沒有方便執行的方法，則管理及儲存各種網域的記錄可能會變得相當麻煩。

IBM Cloud DNS 提供客戶一個集中位置，透過使用我們的基本 DNS 管理介面來檢視及管理其網域。它也提供選項讓使用者能夠在相同位置管理反向 DNS 及次要 DNS，且完全免費。

IBM Cloud 也提供一套額外的[網路工具](/docs/infrastructure/network-tools?topic=network-tools-gettingstarted-with-network-tools#gettingstarted-with-network-tools)。如需透過[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 使用我們 DNS 介面的特定指示，請參閱[如何使用 DNS 介面](/docs/infrastructure/dns?topic=dns-how-to-use-the-dns-interface)。

## 如何運作
{: #how-dns-works}

在基本層次上，{{site.data.keyword.BluSoftlayer_notm}} DNS 的運作方式與您所使用的任何 DNS 管理工具類似。您可以與現有的 DNS 記錄進行互動及編輯，新增記錄，以及更新反向 DNS 的相關資訊。在另一個 DNS 管理服務上使用 {{site.data.keyword.BluSoftlayer_notm}} 或甚至自行管理它，其主要好處是您會有一個集中的可靠位置來儲存所有資料。

作為一項附加服務，{{site.data.keyword.BluSoftlayer_notm}} 可免費提供次要 DNS 區域給我們的客戶，讓使用者能夠備份其主要 DNS 記錄，以防萬一發生資料流失或節點失效。

## 如何管理 DNS
{: #how-to-manage-dns}

大部分使用者都使用[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 來管理其主要、反向及次要 DNS。入口網站是我們的點按方式介面，能管理 DNS 的一切。

您也可以選擇使用 IBM Cloud SoftLayer API (SLAPI) 進行 DNS 互動。API 的功能與我們的「入口網站使用者介面」幾乎相同。不過，如果您要大量編輯 DNS 記錄，則「客戶入口網站」可提供最多 20 筆的大量作業設定，而 API 則能提供更大的彈性。如需使用 SLAPI 與 DNS 互動的相關資訊，請參閱[此 API 文件](/docs/infrastructure/dns?topic=dns-getting-started-with-the-dns-api#getting-started-with-the-dns-api)。


