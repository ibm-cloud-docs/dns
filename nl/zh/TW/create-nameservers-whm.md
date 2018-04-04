---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 在 Cpanel/WHM 中建立您自己的名稱伺服器

這篇文章提供如何使用 Web Host Manager (WHM) 建立您自己的名稱伺服器的步驟。在遵循下列步驟之後，如果您遇到問題，請參考本文章來提交支援問題單。

1. 首先，決定您的名稱伺服器的名稱。例如，假設我的代管公司名稱為 "Awesome Server Hosting"，因此我想設定 `ns1.awesomeserverhosting.com` 和 `ns2.awesomeserverhosting.com`。

* 在瀏覽器中移至 https://XX.XX.XX.XX:2087，以登入您伺服器上的 WHM。

* 若要設定您的名稱伺服器，請選取左側列中的第一個選項，其應該為「基本 cPanel/WHM 設定」。 

 * 在這裡，您可以設定主要、次要、第三層及第四層名稱伺服器的名稱。

 * 完成時，請選取「儲存」按鈕。

2. 現在，在我的伺服器中建立 "awesomeserverhosting.com" 的區域檔案。有兩種方式可執行這項作業：

第一個方法：建立 "awesomeserverhosting.com" 的網域帳戶。關於這項作業的指示不屬於本文章的範圍，如需相關資訊，請參閱 [cPanel 文件](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)： 

   * 在左側資訊看板中，選取「DNS 功能」下的「新增 DNS 區域」。

   * 提供管理 "awesomeserverhosting.com" 的主要網站的 IP 位址，當然還有網域名稱。

   **附註：當您不打算在此伺服器上管理 `awesomeserverhosting.com` 時，才需要這麼做！**

   * 在**網路設定**標題下，按一下**名稱伺服器 IP**。

   * 提供名稱伺服器的名稱。例如，提交 `ns1.awesomeserverhosting.com`，然後提交 `ns2.awesomeserverhosting.com`。

   * 在左側列中，尋找位於**服務配置**下的**名稱伺服器設定**。

   * 將會顯示類似這樣的訊息：「建議您不要啟用名稱伺服器，除非您要使用它。如果您想要停用名稱伺服器，您可以隨時在服務管理程式中關閉它。」

   * 現在讓我們的名稱伺服器啟動和執行，因此請選取標示為**繼續 >>**的按鈕。`cPanel` 工具將確保您將適當的套件安裝至伺服器，並確定這些套件已配置為可適當地運作，以管理您的名稱服務。現在已全部設定妥當！

外部鏈結：

* [cPanel 文件](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
