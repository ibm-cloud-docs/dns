---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

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


# 管理次要 DNS 區域
{: #manage-secondary-dns-zones}

{{site.data.keyword.cloud}} 提供「次要 DNS」給所有客戶，作為萬一資料流失時快取主要 DNS 區域的方法。維護「次要 DNS 區域」並非必要，但強烈建議具有多個網域的使用者這麼做。 


## 新增次要 DNS 區域
{:#add-a-secondary-dns-zone}

請遵循下列步驟來新增「次要 DNS 區域」：

* 在 [{{site.data.keyword.cloud_notm}} 主控台 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 中導覽至**次要 DNS 區域**畫面，方法是從導覽功能表選取**標準基礎架構**。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 次要區域**。
* 選取**新增區域**標籤。
* 在**區域**欄位中，輸入**區域的網域**。
* 在**主要名稱伺服器**欄位中，輸入**主要名稱伺服器的 IP 位址**。
* 在**傳送間隔**欄位中，輸入主要 DNS 區域將傳送至次要 DNS 區域的**傳送時間**（分鐘）。
* 選取**新增**按鈕來新增區域，或選取**取消**來取消動作。

### 新增之後的後續情形
{:#add-a-secondary-dns-zone-next}

建立「次要 DNS 區域」之後，它會出現在「次要 DNS 區域」畫面的「區域」清單中。將資料從「主要區域」傳送至「次要區域」時，會依您在建立區域時指定的間隔來進行。您可以隨時對「區域」進行[編輯](#edit-a-secondary-dns-zone)、[手動傳送](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone)或[轉換](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone)至「主要區域」。也可以隨時[刪除](#delete-a-secondary-dns-zone)「次要 DNS 區域」。

## 編輯次要 DNS 區域
{:#edit-a-secondary-dns-zone}

可隨時編輯「次要 DNS 區域」，以更新「主要名稱伺服器」或「傳送間隔」。請遵循下列步驟，以編輯「次要 DNS 區域」。

* 在 [{{site.data.keyword.cloud_notm}} 主控台 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 中導覽至**次要 DNS 區域**畫面，方法是從導覽功能表選取**標準基礎架構**。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 次要區域**。
* 按一下**包含次要 DNS 區域的列**的任意處來開啟區域以進行編輯。如果有多個「次要區域」，可以過濾視圖，以找出需要編輯的「區域」。
  {:note}  
* 必要的話，可更新**主要名稱伺服器**及**傳送間隔**欄位。
* 選取**更新**按鈕來更新「次要 DNS 區域」，或選取**取消**來取消動作。

### 編輯之後的後續情形
{:#edit-a-secondary-dns-zone-next}

編輯「次要 DNS 區域」之後，**主要名稱伺服器**及**傳送間隔**值將反映更新內容，而「次要區域」將根據新資訊開始接收傳送。任何時候，只要重複先前步驟，即可再次編輯「區域」。

## 刪除次要 DNS 區域
{:#delete-a-secondary-dns-zone}

建立「次要 DNS 區域」之後，可以隨時刪除它。請注意，如果刪除「次要 DNS 區域」，就無法擷取它。請遵循下列步驟，以刪除「次要 DNS 記錄」。

 * 在 [{{site.data.keyword.cloud_notm}} 主控台 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 中導覽至**次要 DNS 區域**畫面，方法是從導覽功能表選取**標準基礎架構**。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 次要區域**。
* 對於需要刪除的區域，從**動作**下拉清單中選取**刪除**。即會出現蹦現確認框。
  如果有多個「次要區域」，可以過濾視圖，以找出要刪除的「區域」。
  {:note}
* 選取**是**按鈕來確認刪除，或選取**否**按鈕來取消此動作。

### 刪除之後的後續情形
{:#delete-a-secondary-dns-zone-next}

刪除「次要 DNS 區域」之後，從「主要區域」執行的自動傳送將停止，且「次要區域」將不再存在。如果「主要區域」隨時需要「次要 DNS 區域」，則[可以建立新的次要 DNS 區域](#add-a-secondary-dns-zone)。
