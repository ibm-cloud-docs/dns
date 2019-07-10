---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone Record, Update DNS Zone Record, edit dns zone record, add dns zone record, delete dns zone record 

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 管理 DNS 區域記錄
{: #manage-dns-zone-records}
本節詳細說明如何新增、編輯和刪除 DNS 區域記錄。

## 新增 DNS 區域記錄
{: #add-a-dns-zone-record}

在[新增 DNS 區域](/docs/infrastructure/dns?topic=dns-manage-dns-zones#add-a-dns-zone)之後，記錄可隨時新增至該區域。這些記錄包括：

* A（主機）記錄
* AAAA（主機）記錄
* CNAME（別名）記錄
* MX（郵件交換）記錄
* TXT（文字）記錄
* SRV（服務）記錄

請遵循下列步驟以新增「DNS 區域記錄」：

* 導覽至 **DNS 區域**畫面。請參閱[使用 DNS 區域畫面](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)。
* 選取將新增記錄的「DNS 區域」。
* 從**資源類型**下拉清單中，選取想要的**資源類型**。
* 完成新「記錄」的其餘欄位。如需相關資訊，請參閱下表：<br/><br/><table border="1"><tbody><tr><th scope="col">記錄類型</th><th scope="col">欄位</th><th scope="col">項目</th></tr><tr><td rowspan="3">A（主機）、AAAA（主機）或 CNAME（別名）</td><td>主機</td><td>輸入<strong>主機名稱</strong>。</td></tr><tr><td>指向</td><td>輸入「主機記錄」指向的 <strong>IP 位址</strong>。</td></tr><tr><td>TTL</td><td>從下拉清單中選取「存活時間 (TTL)」。TTL 預設為 15 分鐘。</td></tr><tr><td rowspan="4">MX（郵件交換）</td><td>優先順序</td><td>輸入目標主機的<strong>優先順序</strong>。數字越低，優先順序越高。</td></tr><tr><td>主機</td><td>輸入<strong>主機名稱</strong>。</td></tr><tr><td>執行</td><td>輸入郵件伺服器的 <strong>CNAME</strong>。這通常是以 `mail.example.com` 來表示。</td></tr><tr><td>TTL</td><td>從下拉清單中選取「存活時間 (TTL)」。TTL 預設為 15 分鐘。</td></tr><tr><td rowspan="3">TXT（文字）</td><td>名稱</td><td>輸入 <strong>@</strong> 或<strong>網域名稱</strong>。</td></tr><tr><td>值</td><td>輸入<strong>記錄</strong>，以驗證網域或 IP 的適當電子郵件結束權限。</td></tr><tr><td>TTL</td><td>從下拉清單中選取「存活時間 (TTL)」。TTL 預設為 15 分鐘。</td></tr><tr><td rowspan="8">SRV（服務記錄）</td><td>服務</td><td>輸入所需服務的<strong>符號名稱</strong>。</td></tr><tr><td>通訊協定</td><td>從下拉清單中選取要使用的<strong>通訊協定</strong>。</td></tr><tr><td>優先順序</td><td>輸入目標主機的<strong>優先順序</strong>。數字越低，優先順序越高。</td></tr><tr><td>加權</td><td>針對具有相同優先順序的記錄，輸入<strong>相對加權</strong>。</td></tr><tr><td>埠</td><td>請輸入要在其中找到該服務的 <strong>TCP 或 UPD 埠</strong>。</td></tr><tr><td>主機（選用）</td><td>輸入服務的<strong>主機名稱</strong>。</td></tr><tr><td>目標</td><td>輸入提供服務之機器的<strong>標準主機名稱</strong>。</td></tr><tr><td>TTL</td><td>從下拉清單中選取「存活時間 (TTL)」。TTL 預設為 15 分鐘。</td></tr></tbody></table><br/>
* 選取**新增記錄**按鈕，以新增新的「區域記錄」。

### 後續情形
{:#add-a-dns-zone-record-next}

新增「區域記錄」之後，它會出現在畫面的**現有記錄**區段中。您可以隨時[編輯](#edit-a-dns-zone-record)或[刪除](#delete-a-dns-zone-record)「區域記錄」。

## 編輯 DNS 區域記錄
{: #edit-a-dns-zone-record}

使用者可以編輯現有的「DNS 區域記錄」來更新不同區域，例如「存活時間 (TTL)」、「指標 (PTR)」記錄和「主機名稱」。多個主機及別名可在任何時間與「DNS 區域記錄」相關聯。請遵循下列步驟來編輯現有的「DNS 區域記錄」。

* 從導覽功能表選取**標準基礎架構**，以導覽至想要的 **DNS 區域**畫面。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 正向區域**。
* 按一下包含任何現有記錄的**列**。 

  以斜體字表示的記錄無法編輯。這些通常侷限於 NS（名稱伺服器）記錄。
  {: note}
  
* 視需要更新記錄的詳細資料。
* 選取**更新**按鈕以更新記錄，或選取**取消**來取消動作。

### 後續情形
{: #edit-a-dns-zone-record-next}

更新記錄時，其詳細資料會自動顯示新項目。可隨時更新記錄，可刪除現有的記錄，也可[新增](#add-a-dns-zone-record)新記錄。

## 刪除 DNS 區域記錄
{: #delete-a-dns-zone-record}

刪除 DNS 區域記錄是透過 **DNS 編輯區域**畫面執行。刪除 DNS 區域記錄的作業無法復原。
* 在「DNS 區域」清單中按一下名稱，以選取具有您要刪除之記錄的 DNS 區域。
* 在包含所要記錄之列的尾端選取「刪除」圖示。即會出現蹦現確認框。
* 選取**是**按鈕來確認刪除，或選取**否**按鈕來取消此動作。
