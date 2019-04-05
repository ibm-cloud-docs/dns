---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Master Nameserver

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 編輯次要 DNS 區域
{:#edit-a-secondary-dns-zone}

可隨時編輯「次要 DNS 區域」，以更新「主要名稱伺服器」或「傳送間隔」。請遵循下列步驟，以編輯「次要 DNS 區域」。

* 在[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 中導覽至**次要 DNS 區域**畫面，方法是從導覽功能表選取**標準基礎架構**。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 次要區域**。
* 按一下**包含次要 DNS 區域的列**的任意處來開啟區域以進行編輯。如果有多個「次要區域」，可以過濾視圖，以找出需要編輯的「區域」。
  {:note}  
* 必要的話，可更新**主要名稱伺服器**及**傳送間隔**欄位。
* 選取**更新**按鈕來更新「次要 DNS 區域」，或選取**取消**來取消動作。

## 後續情形
{:#edit-a-secondary-dns-zone-next}

編輯「次要 DNS 區域」之後，**主要名稱伺服器**及**傳送間隔**值將反映更新內容，而「次要區域」將根據新資訊開始接收傳送內容。任何時候，只要重複上述步驟，即可再次編輯「區域」。
