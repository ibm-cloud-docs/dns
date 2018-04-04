---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 新增次要 DNS 區域

{{site.data.keyword.BluSoftlayer_notm}} 提供「次要 DNS」給所有客戶，作為萬一資料流失時快取主要 DNS 區域的方法。維護「次要 DNS 區域」並非必要，但強烈建議具有多個網域的使用者這麼做。請遵循下列步驟來新增「次要 DNS 區域」：

* 導覽至[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 中的**次要 DNS 區域**畫面。請參閱[使用 DNS 區域畫面](use-dns-zones-screen.html){:new_window}。
* 選取**新增區域**標籤。
* 在**區域**欄位中，輸入**區域的網域**。
* 在**主要名稱伺服器**欄位中，輸入**主要名稱伺服器的 IP 位址**。
* 在**傳送間隔**欄位中，輸入主要 DNS 區域將傳送至次要 DNS 區域的**傳送時間**（分鐘）。
* 選取**新增**按鈕來新增區域，或選取**取消**來取消動作。

## 後續情形

建立「次要 DNS 區域」之後，它會出現在「次要 DNS 區域」畫面的「區域」清單中。將資料從「主要區域」傳送至「次要區域」時，會依您在建立區域時指定的間隔來進行。您可以隨時對「區域」進行[編輯](edit-secondary-dns-zone.html)、[手動傳送](make-manual-zone-transfer-secondary-dns.html)或[轉換](convert-secondary-dns-zone-primary-zone.html)至「主要區域」。也可以隨時[刪除](delete-secondary-dns-zone.html)「次要 DNS 區域」。
