---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 將次要 DNS 區域轉換成主要區域
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

[次要 DNS 區域](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window}可以隨時轉換成「主要」區域。當您將「次要 DNS 區域」轉換成「主要」時，{{site.data.keyword.BluSoftlayer_notm}} 名稱伺服器會變成已轉換區域的主名稱伺服器。請遵循下列步驟，將「次要 DNS 區域」轉換成「主要」：

* 在[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 中導覽至**次要 DNS 區域**畫面，方法是從導覽功能表選取**標準基礎架構**。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 次要區域**。
* 針對所要的「次要區域」，從**動作**下拉清單中選取**轉換成主要**。
* 選取**是**按鈕來轉換區域，或選取**否**來取消動作。

## 後續情形
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

將「次要 DNS 區域」轉換成「主要」之後，您可以在**正向區域**畫面上檢視它。該「區域」先前已存在的所有 SOA 及 NS 記錄，將取代為 {{site.data.keyword.BluSoftlayer_notm}} SOA 及 NS 記錄（無法編輯）。您仍然可以[編輯其餘的區域記錄](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)。
