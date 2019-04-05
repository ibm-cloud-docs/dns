---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Record PTR, IP addresses, Reverse DNS feature

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 新增或編輯 PTR（指標）記錄
{:#add-or-edit-a-ptr-pointer-record}

PTR 或指標記錄將 IP 位址解析成主機名稱。使用者可以使用[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/){:new_window} 上的「反向 DNS」功能，來新增要與 IP 位址相關聯的「PTR 記錄」。此外，也可以利用新增「PTF 記錄」的相同方式來編輯它們。請遵循下列步驟，以新增或編輯裝置的「PTR 記錄」：

* 針對將接收來自**裝置清單**之「PTR 記錄」的裝置，擷取**公用 IP 位址**。
* 在[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 中顯示**反向 DNS 記錄**畫面，方法是從導覽功能表選取**標準基礎架構**。 
* 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 反向 DNS**。
* 在**視圖 IP**欄位中，輸入從「裝置清單」中擷取的**公用 IP 位址**。
* 在包含**反向記錄**詳細資料的該列的任何位置按一下，以開啟該列來編輯。
* 根據下表，完成或更新「記錄」的欄位：<br/><br/><table border="1"><tbody><tr><th>欄位</th><th>項目</th></tr><tr><td>反向 DNS</td><td>IP 位址將解析成的主機名稱。</td></tr><tr><td>反向 TTL</td><td>新記錄的存活時間 (TTL)</td></tr><tr><td>附註</td><td>關於記錄的任何適用附註</td></tr></tbody></table><br/>
* 按一下**更新**按鈕來更新記錄。按一下**取消**即可取消動作。

## 後續情形
{:#add-or-edit-a-ptr-pointer-record-next}

新增「PTR 記錄」之後，與該記錄相關聯的「公用 IP 位址」會解析成記錄中所指定的主機名稱。可以隨時編輯記錄。若要從「PTR 記錄」中移除詳細資料，請使用**編輯**程序來刪除欄位中的所有資訊。
