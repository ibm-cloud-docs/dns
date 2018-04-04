---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 將次要 DNS 區域轉換成主要區域

[次要 DNS 區域](add-secondary-dns-zone.html){:new_window}可以隨時轉換成「主要」區域。當您將「次要 DNS 區域」轉換成「主要」時，{{site.data.keyword.BluSoftlayer_notm}} 名稱伺服器會變成已轉換區域的主名稱伺服器。請遵循下列步驟，將「次要 DNS 區域」轉換成「主要」：

* 導覽至[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 中的**次要 DNS 區域**畫面。請參閱[使用 DNS 區域畫面](use-dns-zones-screen.html){:new_window}。
* 針對所要的「次要區域」，從**動作**下拉清單中選取**轉換成主要**。
* 選取**是**按鈕來轉換區域，或選取**否**來取消動作。

## 後續情形

將「次要 DNS 區域」轉換成「主要」之後，您可以在**轉遞區域**畫面上檢視它。該「區域」先前已存在的所有 SOA 及 NS 記錄，將取代為 {{site.data.keyword.BluSoftlayer_notm}} SOA 及 NS 記錄（無法編輯）。您仍然可以[編輯其餘的區域記錄](edit-dns-zone-record.html)。
