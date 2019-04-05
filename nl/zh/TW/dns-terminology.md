---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Terminology, Caching, individual DNS servers, DNS resolver

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS 術語
{:#dns-terminology}

## 快取及存活時間
{:#caching-and-time-to-live}

因為系統（如 DNS）產生大量要求，所以設計者提供了一種機制來減少個別 DNS 伺服器的負載，如下所示：

當 DNS 解析器（亦即用戶端）接收 DNS 回應時，它會快取該回應長達一段給定的時間，稱之為存活時間，或 TTL。TTL 的值是由給予該回應的 DNS 伺服器的管理者設定。在回應進入快取之後，解析器會查看其快取（已儲存）回應；只有當 TTL 到期（或管理者從解析器的記憶體中手動清除回應時），解析器才會聯絡 DNS 伺服器來索取相同資訊。

## 授權開始 (SOA) 記錄參數
{:#soa-record-parameters}

一般而言，存活時間是指定在「授權開始 (SOA)」記錄中。SOA 參數如下：

### 序號
{:#soa-record-parameters-serial}

此區域檔案的修訂號碼。每次變更區域檔案時都增加此號碼，以便將變更分送至任何次要 DNS 伺服器。

### 重新整理
{:#soa-record-parameters-refresh}

次要名稱伺服器應該等待從網域的主要名稱伺服器檢查 DNS 區域新副本的時間量（以秒為單位）。如果區域檔案已變更，則次要 DNS 伺服器會更新其區域副本，以符合主要 DNS 伺服器的區域。

### 重試
{:#soa-record-parameters-retry}

如果嘗試再次以次要名稱伺服器重新整理網域區域之前該次要名稱伺服器嘗試重新整理失敗，則網域的主要名稱伺服器應該等待的時間量（以秒為單位）。

### 到期
{:#soa-record-parameters-expire}

次要名稱伺服器不再被視為主伺服器之前保留區域的時間量（以秒為單位）。

### 最小值
{:#soa-record-parameters-minimum}

網域資源記錄有效的時間量（以秒為單位）。這也稱為最小 TTL，且可由個別資源記錄的 TTL 置換。

### TTL（存活時間）
{:#soa-record-parameters-ttl}

在到期及回到主名稱伺服器之前，在本端快取網域名稱以取得更新資訊的秒數。
