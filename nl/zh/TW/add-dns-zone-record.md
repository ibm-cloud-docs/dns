---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone Record, TTL Select, Relative Weight

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 新增 DNS 區域記錄
{:#add-a-dns-zone-record}

在[新增 DNS 區域](/docs/infrastructure/dns?topic=dns-add-a-dns-zone)之後，記錄可隨時新增至該區域。這些記錄包括：

* A（主機）記錄
* AAAA（主機）記錄
* CNAME（別名）記錄
* MX（郵件交換）記錄
* TXT（文字）記錄
* SRV（服務）記錄

請遵循下列步驟以新增「DNS 區域記錄」：

* 導覽至想要的 **DNS 區域**畫面。請參閱[使用 DNS 區域畫面](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)。
* 選取將新增記錄的「DNS 區域」。
* 從**資源類型**下拉清單中，選取想要的**資源類型**。
* 完成新「記錄」的其餘欄位。如需相關資訊，請參閱下表：<br/><br/><table border="1"><tbody><tr><th scope="col">記錄類型</th><th scope="col">欄位</th><th scope="col">項目</th></tr><tr><td rowspan="3">A（主機）、AAAA（主機）或 CNAME（別名）</td><td>主機</td><td>輸入<strong>主機名稱</strong>。</td></tr><tr><td>指向</td><td>輸入「主機記錄」指向的 <strong>IP 位址</strong>。</td></tr><tr><td>TTL</td><td>從下拉清單中選取「存活時間 (TTL)」。TTL 預設為 15 分鐘。</td></tr><tr><td rowspan="4">MX（郵件交換）</td><td>優先順序</td><td>輸入目標主機的<strong>優先順序</strong>。數字越低，優先順序越高。</td></tr><tr><td>主機</td><td>輸入<strong>主機名稱</strong>。</td></tr><tr><td>執行</td><td>輸入郵件伺服器的 <strong>CNAME</strong>。這通常是以 mail.example.com 來表示。</td></tr><tr><td>TTL</td><td>從下拉清單中選取「存活時間 (TTL)」。TTL 預設為 15 分鐘。</td></tr><tr><td rowspan="3">TXT（文字）</td><td>名稱</td><td>輸入 <strong>@</strong> 或<strong>網域名稱</strong>。</td></tr><tr><td>值</td><td>輸入<strong>記錄</strong>，以驗證網域或 IP 的適當電子郵件結束權限。</td></tr><tr><td>TTL</td><td>從下拉清單中選取「存活時間 (TTL)」。TTL 預設為 15 分鐘。</td></tr><tr><td rowspan="8">SRV（服務記錄）</td><td>服務</td><td>輸入所需服務的<strong>符號名稱</strong>。</td></tr><tr><td>通訊協定</td><td>從下拉清單中選取要使用的<strong>通訊協定</strong>。</td></tr><tr><td>優先順序</td><td>輸入目標主機的<strong>優先順序</strong>。數字越低，優先順序越高。</td></tr><tr><td>加權</td><td>針對具有相同優先順序的記錄，輸入<strong>相對加權</strong>。</td></tr><tr><td>埠</td><td>請輸入要在其中找到該服務的 <strong>TCP 或 UPD 埠</strong>。</td></tr><tr><td>主機（選用）</td><td>輸入服務的<strong>主機名稱</strong>。</td></tr><tr><td>目標</td><td>輸入提供服務之機器的<strong>標準主機名稱</strong>。</td></tr><tr><td>TTL</td><td>從下拉清單中選取「存活時間 (TTL)」。TTL 預設為 15 分鐘。</td></tr></tbody></table><br/>
* 選取**新增記錄**按鈕，以新增新的「區域記錄」。

## 後續情形
{:#add-a-dns-zone-record-next}

新增「區域記錄」之後，它會出現在畫面的**現有記錄**區段中。您可以隨時[編輯](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)或[刪除](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone)「區域記錄」。
