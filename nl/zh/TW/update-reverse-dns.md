---
copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-02-26"

keywords: Reverse DNS Record, Reverse DNS, IP address, Individual IP Select

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 更新反向 DNS 記錄
{:#update-reverse-dns-record}

反向 DNS 可讓使用者識別與 IP 位址相關聯的網域。客戶可以隨時更新其反向 DNS 記錄，以變更 PTR 及存活時間 (TTL)。在**管理**版本 [IBM Cloud 主控台 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/) 內，您可以利用**搜尋和取代**工具來大量更新 PTR 記錄。此工具可讓您在「搜尋」欄位中輸入部分 PTR 或完整的 PTR，並以所要的資訊取代對應 PTR 內的每一個出現項目。 

請注意，只有當現有的 PTR 與「伺服器」或 VLAN 相關聯時，此工具才會運作。如果 PTR 不存在，則不會列出任何詳細資料，且嘗試更新將導致錯誤。 

若要新增「反向 DNS PTR」記錄，請參閱[新增及編輯 PTR（指標）記錄](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record)。請遵循下列步驟來更新「反向 DNS」記錄：

 * 使用您的唯一認證，導覽至 [IBM Cloud 主控台 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/)。
 * 從導覽功能表選取**標準基礎架構**。
 * 從「標準基礎架構」導覽功能表，選取**網路 > DNS > 反向 DNS**。
 * 鍵入 IP 位址，或從下拉功能表選取它，然後按一下**檢視 IP**。
 * 編輯列出的選項，然後按一下**儲存**。您也可以選擇**編輯這個子網路中的所有 IP 的 RDNS** 以在整個子網路進行變更。 
 

