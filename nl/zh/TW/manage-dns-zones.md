---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 管理 DNS 區域
{: #manage-dns-zones}

## 新增 DNS 區域
{: #add-a-dns-zone}

{{site.data.keyword.cloud}} 的 DNS 管理可延伸至或許不在 {{site.data.keyword.cloud_notm}} 網路上的 DNS 區域。您可以使用我們的介面，隨時新增 DNS 區域（以單一網域新增或大量新增）。新增 DNS 區域的作業目前是在 [IBM Cloud 主控台](https://{DomainName}/)進行。請遵循下列步驟以新增一個以上的「DNS 區域」。

* 使用您的唯一認證，登入 [IBM Cloud 主控台](https://{DomainName}/)。
* 從導覽功能表選取**標準基礎架構**。
* 從**網路**下拉功能表中選取 **DNS**。
* 選取**正向區域**。
* 選取右上方的**新增 DNS 區域**標籤。
* 決定您要新增單一網域或多個網域：

|如果新增...|則...|
|---|---|
|單一網域|在畫面的**新增單一網域**區段中完成下列步驟：<ul><li>在**網域名稱**欄位中輸入**網域名稱**。</li><li>在 **IP 位址**欄位中，輸入網域名稱將指向的 **IP 位址**。</li><li>按一下**新增區域**按鈕，以新增網域。</li></ul>|
|多個網域|決定網域是與單一 IP 位址還是多個 IP 位址相關聯：<ul><li>如果網域將與單一 IP 位址相關聯，<ul><li>在**網域**文字框中，輸入**每一個網域**。</li><li>在**預設 IP 位址**欄位中，輸入 **IP 位址**。</li><li>按一下**新增區域**按鈕來大量新增網域。</li></ul></li><li>如果網域將與多個 IP 位址相關聯，<ul><li>以單一行項目，在**網域**文字框中輸入**每一個網域**及其對應的 **IP 位址**。</li><li>按一下**新增區域**按鈕來大量新增網域。</li></ul></li></ul>


### 後續情形
{:#add-a-dns-zone-next}

順利新增單一區域之後，您會自動被重新導向至「區域編輯」頁面。新的 DNS 區域會出現在 [IBM Cloud 主控台 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 內，[DNS 區域畫面](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)上的「DNS 區域」清單中。可隨時[編輯](#edit-a-dns-zone)或[刪除](#delete-a-dns-zone)區域。

## 編輯 DNS 區域
{: edit-a-dns-zone}
按一下區域的名稱，以在「DNS 區域」畫面的區域清單中選取您要編輯的區域。這會開啟「DNS 編輯區域」頁面。從這裡，您可以變更 DNS 區域，然後按一下**更新 SOA** 來確定變更。 

**編輯 DNS 區域**畫面容許您為您正在編輯的區域新增記錄和編輯現有記錄。您也可以從這個畫面匯出或刪除區域。

### 後續情形
{:#edit-a-dns-zone-next}

請按一下**檢視所有 DNS 區域**，以回到「DNS 區域」清單。


## 刪除 DNS 區域
{: #delete-a-dns-zone}

新增「DNS 區域」之後，可以隨時刪除它。「DNS 區域」的刪除是永久的；您無法復原它們。請遵循下列步驟來刪除 DNS 區域：

* 從導覽功能表選取**標準基礎架構**，以導覽至想要的 **DNS 區域**畫面。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS**，然後選擇您需要的區域類型。
* 在包含所要「DNS 區域」之列的末尾選取**刪除**圖示。即會出現蹦現確認框。
* 選取**是**按鈕來確認刪除，或選取**否**按鈕來取消此動作。

也可以從「編輯 DNS 區域」畫面內刪除區域。
{:tip}

### 後續情形
{:#delete-a-dns-zone-next}

刪除「DNS 區域」之後，就無法再使用 [IBM Cloud 主控台 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 來管理它。若要重新管理儀表板中已刪除的區域，必須將其[新增為新區域](#add-a-dns-zone)。
