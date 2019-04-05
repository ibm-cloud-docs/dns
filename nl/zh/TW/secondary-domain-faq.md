---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-07"

keywords: Secondary Domain FAQ, zone transfers, IBM Cloud DNS servers

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 次要網域常見問題
{:#secondary-domain-faq}

## 哪些 IBM Cloud DNS 伺服器會回應次要網域？
{:#what-ibm-cloud-dns-servers-will-answer-for-my-secondary-domains}

IBM Cloud 的 Anycast、已啟用 IPv6 的主 DNS 伺服器：

 * ns1.softlayer.com
 * ns2.softlayer.com

## 區域傳送來自何處？
{:#where-will-the-zone-transfers-come-from}

次要網域的傳送將來自這四個 IP 位址的其中之一：

  * 66.228.118.67
  * 67.228.119.235
  * 208.43.119.235
  * 12.96.161.249

## 傳送網域之後，網域或它的變更需要多久的時間才看得見？
{:#how-long-does-it-take-for-changes-to-become-visible}

當傳送完成之後，網域及它的任何變更將立即出現在 IBM Cloud DNS 伺服器上。由於 DNS 的快取和傳播本質，可能需要一些時間才能讓這些變更出現在其他 DNS 伺服器上。  

## 是否支援區域更新通知？
{:#are-zone-update-notifies-supported}

目前不支援通知。

## 「立即傳送」按鈕的速度有多快？
{:#how-immediate-is-the-transfer-now-button}

按一下立即傳送按鈕之後，該網域將在下一分鐘開始時傳送。

## 主節點是否可配置在專用網路上，或者它必須透過公用網路進行？
{:#can-a-master-be-configured-on-private-network}

目前不行。所有 AXFR 要求都透過公用網路進行。

## 在主節點無法使用的天數之後移除從屬節點嗎？
{:#are-slaves-removed-after-days-master-is-unavailable}

如果網域的主節點關閉或配置錯誤長達一段很長的時間，我們將會停止嘗試傳送該網域。入口網站會提供客戶意見（「錯誤訊息」標籤），而萬一傳送區域時發生問題而停用網域，入口網站還提供方法來重新啟動網域（「手動區域傳送」標籤）。

## 1 分鐘是否為最低傳送頻率？
{:#is-1minute-lowest-transfer-frequency}

是。

## 如果頻率是設為 1920 分鐘，然後回到 10，則 1920 分鐘是否必須先到期，然後新頻率才會生效？
{:#frequency-change-expiration-effects}

否。系統會計算重新傳送佇列，把前次嘗試傳送的時間加上它的頻率。因此，如果您的頻率是設為 1920，然後您將它變更為 10 分鐘，則只要前次嘗試傳送之後已超過 10 分鐘，我們就會立即重試，然後再每隔 10 分鐘重試。
