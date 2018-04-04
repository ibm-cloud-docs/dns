---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 更新反向 DNS 記錄

反向 DNS 可讓使用者識別與 IP 位址相關聯的網域。客戶可以隨時更新其反向 DNS 記錄，以變更 PTR 及存活時間 (TTL)。在**管理**版本[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 內，您可以利用**搜尋和取代**工具來大量更新 PTR 記錄。此工具可讓您在「搜尋」欄位中輸入部分 PTR 或完整的 PTR，並以所要的資訊取代對應 PTR 內的每一個出現項目。 

請注意，只有當現有的 PTR 與「伺服器」或 VLAN 相關聯時，此工具才會運作。如果 PTR 不存在，則不會列出任何詳細資料，且嘗試更新將導致錯誤。 

若要新增「反向 DNS PTR」記錄，請參閱[新增及編輯 PTR（指標）記錄](add-and-edit-ptr-pointer-record.html)。請遵循下列步驟來更新「反向 DNS」記錄：

 * 使用您的唯一認證，導覽至[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/)。
 * 從**網路**下拉功能表中選取 **DNS**。
 * 選取**反向 DNS** 功能表選項。
 * 判定是必須對所有對應的 IP 位址網路 VLAN 進行更新，或是對個別 IP 進行變更。<br><br><table border="1"><tbody><tr><th>如果要進行更新的對象是...</th><th>則...</th></tr><tr><td>個別 IP</td><td><ul><li>選取<b>下拉功能表</b>以查看 IP 位址</li><li>按一下所需的 <strong>IP 位址</strong>，以檢視與「伺服器」相關聯的「反向 DNS」詳細資料。</li></ul></td></tr><tr><td>在「網路 VLAN」上的所有對應 IP 位址</td><td><ul><li>如上所述選取 IP 之後，選取<strong>檢視 IP</strong> 選項。</li><li>選取<strong>編輯這個子網路中的所有 IP 的 RDNS</strong> 選項。</li></ul></td></tr></tbody></table><br/>
 * 針對個別 IP，只要新增**主機名稱**和**反向 TTL**，然後選取**儲存**。對於整個**子網路**，則強調顯示**反向 DNS**直欄之下的開放空間，並新增**主機名稱**，然後選取**更新**按鈕。必須針對「子網路」中的每個 IP 位址完成此作業。
