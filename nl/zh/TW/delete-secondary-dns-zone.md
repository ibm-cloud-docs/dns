---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 刪除次要 DNS 區域
{:#delete-a-secondary-dns-zone}

建立「次要 DNS 區域」之後，可以隨時刪除它。請注意，如果刪除「次要 DNS 區域」，就無法擷取它。請遵循下列步驟，以刪除「次要 DNS 記錄」。

 * 在[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 中導覽至**次要 DNS 區域**畫面，方法是從導覽功能表選取**標準基礎架構**。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 次要區域**。
* 對於需要刪除的區域，從**動作**下拉清單中選取**刪除**。即會出現蹦現確認框。
  如果有多個「次要區域」，可以過濾視圖，以找出要刪除的「區域」。
  {:note}
* 選取**是**按鈕來確認刪除，或選取**否**按鈕來取消此動作。

## 後續情形
{:#delete-a-secondary-dns-zone-next}

刪除「次要 DNS 區域」之後，從「主要區域」執行的自動傳送將停止，且「次要區域」將不再存在。如果「主要區域」隨時需要「次要 DNS 區域」，則[可以建立新的次要 DNS 區域](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone)。
