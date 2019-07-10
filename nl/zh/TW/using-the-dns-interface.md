---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-06-11"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 如何使用 DNS 介面
{:#how-to-use-the-dns-interface}

請遵循下列步驟，透過 {{site.data.keyword.cloud}} 基礎架構客戶入口網站使用 DNS 介面：

* 導覽至[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/)。
* 從導覽功能表選取**標準基礎架構**。
* 選取**網路->DNS->正向區域**
* 選取您要管理的「網域」，或選取頁面右側的**新增 DNS 區域**按鈕。

## DNS 介面概觀
{:#dns-interface-overview}
在客戶入口網站的「DNS 介面」中工作，您將具備管理 DNS 所有層面的全部能力。您可以使用畫面頂端的靜態功能表列，從介面的任何畫面中執行每種類型的 DNS 管理。

## 管理 DNS
{:#manage-dns}
在呼叫到入口網站中的 DNS 介面時，您會直接進到**管理 DNS** 畫面，它可讓您檢視、編輯或刪除與您的帳戶相關聯的任何現有主要 DNS。

* 若要新增記錄，只要填寫**新增記錄**下所提供的欄位，然後按一下**新增記錄**按鈕即可。
* 若要修改現有的記錄，請按一下含有該記錄的那一行，它將轉換成**編輯**模式。將設定變更為所要的值，然後按一下**更新**。
* 若要刪除記錄，請選取記錄右側的紅色圓圈，然後在出現提示時按一下**是**。

## 次要 DNS
{:#secondary-dns}

* 導覽至[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/)。
* 從導覽功能表選取**標準基礎架構**。
* 選取**網路->DNS->次要區域**

從此畫面中，您可以新增或修改次要 DNS 設定。

* 若要新增記錄，請選取**新增區域**，並填寫欄位，然後選取**新增**。
* 若要移除次要 DNS 記錄，或將它轉換為主要記錄，請使用頁面右側的**動作**下拉清單，並選擇適當的選項。

## 反向 DNS
{:#reverse-dns}

請遵循下列步驟，透過「入口網站」導覽來使用 DNS 介面：

* 導覽至[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/)。
* 從導覽功能表選取**標準基礎架構**。
* 選取**網路->DNS->反向記錄**
* 在下拉功能表中，選取或輸入您要變更其「反向 DNS」的 IP 位址，然後選取**檢視 IP**
  * 若要新增記錄，請輸入要用於反向 DNS 項目的主機名稱
  * 設定記錄的 TTL（存活時間）。
  * 在您確定資訊之後，請選取**儲存**。

您可以按一下頁面右側的**編輯這個子網路中的所有 IP 的 RDNS**，來修改整個子網路。

* 從這個頁面中，選取您要更新的 IP 的那一行
* 在欄位中輸入資訊，然後選取**更新**。「附註」欄位是選用的。

<!--## Propagation Check

* Navigate to the [customer portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network >Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
