---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone, DNS management, Add DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 新增 DNS 區域
{:#add-a-dns-zone}

{{site.data.keyword.BluSoftlayer_notm}} 的 DNS 管理可延伸至或許不在 {{site.data.keyword.BluSoftlayer_notm}} 網路上的 DNS 區域。您可以使用我們的介面，隨時新增 DNS 區域（以單一網域新增或大量新增）。新增 DNS 區域目前是在「客戶入口網站」的[控制](https://control.softlayer.com/)版本中進行。請遵循下列步驟以新增一個以上的「DNS 區域」。

* 使用您的唯一認證登入「客戶入口網站」的[控制](https://control.softlayer.com/)版本。
* 從導覽功能表選取**標準基礎架構**。
* 從**網路**下拉功能表中選取 **DNS**。
* 選取**正向區域**。
* 選取右上方的**新增 DNS 區域**標籤。
* 決定您要新增單一網域或多個網域：<br> <br><table border="1"><tbody><tr><th>如果新增...</th><th>則...</th></tr><tr><td>單一網域</td><td>在畫面的<strong>新增單一網域</strong>區段中完成下列步驟：<br> <ul><li>在<strong>網域名稱</strong>欄位中輸入<strong>網域名稱</strong>。</li><li>在 <strong>IP 位址</strong>欄位中，輸入網域名稱將指向的 <strong>IP 位址</strong>。</li><li>按一下<strong>新增區域</strong>按鈕，以新增網域。<br> </li></ul></td></tr><tr><td>多個網域</td><td>決定網域是與單一 IP 位址還是多個 IP 位址相關聯：<br> <p> </p><p> </p><p> </p><p> </p><ul><li>如果網域將與單一 IP 位址相關聯，<ul><li>在<strong>網域</strong>文字框中，輸入<strong>每一個網域</strong>。</li><li>在<strong>預設 IP 位址</strong>欄位中，輸入 <strong>IP 位址</strong>。</li><li>按一下<strong>新增區域</strong>按鈕來大量新增網域。</li></ul></li><li>如果網域將與多個 IP 位址相關聯，<ul><li>以單一行項目，在<strong>網域</strong>文字框中輸入<strong>每一個網域</strong>及其對應的 <strong>IP 位址</strong>。</li><li>按一下<strong>新增區域</strong>按鈕來大量新增網域。</li></ul></li><li> </li></ul></td></tr></tbody></table>

## 後續情形
{:#add-a-dns-zone-next}

新增「DNS 區域」之後，它會出現在[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 內，[DNS 區域畫面](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)上的「DNS 區域」清單中。可隨時[編輯](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)或[刪除](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone)區域。


