---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Delete Custom Name Servers, Lock Domain Select, Domain Domains

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 新增、編輯或刪除網域的自訂名稱伺服器
{:#add-edit-or-delete-custom-name-servers-for-a-domain}

在 {{site.data.keyword.BluSoftlayer_notm}} 網路上執行的網域最多可指向 5 個自訂名稱伺服器。使用者可以隨時新增、刪除或變更自訂名稱伺服器。請遵循以下步驟來新增、編輯或刪除網域的自訂名稱伺服器：

1. 從瀏覽器中，開啟[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/){: new_window}，並登入您的帳戶。
2. 在「客戶入口網站」導覽中，從導覽功能表選取**標準基礎架構**。
1. 從「標準基礎架構」導覽功能表，選取**服務 > 網域登錄**。
3. 選取想要的**網域名稱**，將網域展開至其 Snapshot 視圖。
4. 從**鎖定網域**中選取**解除鎖定**
5. 在畫面的**自訂名稱伺服器**區域中選取**新增/編輯 NS** 選項。即會出現一個蹦現方框。
6. 請參閱下表，根據所需的作業完成適當的動作：<br/><br/><table border="1"><tbody><tr><th>作業</th><th>動作</th></tr><tr><td>新增自訂名稱伺服器</td><td>在空白欄位中輸入名稱伺服器的主機名稱。</td></tr><tr><td>刪除自訂名稱伺服器</td><td>從適當的「名稱伺服器」欄位中刪除資訊。</td></tr><tr><td>編輯自訂名稱伺服器</td><td>編輯適當的「名稱伺服器」的對應欄位中的詳細資料。</td></tr></tbody></table>
7. 選取**關聯**按鈕來儲存變更，或選取**取消**來取消動作。

## 後續情形
{:#add-edit-or-delete-custom-name-servers-for-a-domain-next}

更新名稱伺服器詳細資料之後，它們會出現在網域的**自訂名稱伺服器**區段之下。您可以隨時更新詳細資料。
