---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Disable Recursion, DNS IBM Cloud DNS servers, BIND configuration file

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 停用 DNS 的遞迴
{:#disable-recursion-for-dns}

依預設，IBM Cloud DNS 伺服器會執行遞迴。遞迴可讓您的 DNS 伺服器聯絡其他 DNS 伺服器，以協助解析其本身無法解析網域的網域名稱。必要時，遞迴可以證明為有用的工具；不過，它也會讓 DNS 伺服器遭到攻擊，而這可能會使 DNS 伺服器完全當掉。系統管理者通常會識別遞迴的需要，並相應地採取動作。否則，最好是停用遞迴。請依照您的作業系統或控制台，遵循下面的步驟來停用 DNS 遞迴。

## 在 Plesk 中停用遞迴
{:#disable-recursion-in-plesk}
* 登入 **Plesk 管理畫面**。
* 選取**工具和設定**。
* 從區段中按一下 **DNS 範本設定**。
* 從 **DNS 遞迴**區段中，選取 **Localnets**。
* 按一下**確定**按鈕。

## 在 Windows Server 2003 和 2008 中停用遞迴
{:#disable-recursion-in-windows-server}

* 使用**開始**功能表中的 **DNS 管理程式**：
  * 按一下**啟動**按鈕。
  * 選取**系統管理工具**。
  * 選取 **DNS**。
* 在**主控台樹狀結構**中您所要的 **DNS 伺服器**上按一下滑鼠右鍵。
* 選取**內容**標籤。
* 按一下**伺服器選項**區段中的**進階**按鈕。
* 選取**停用遞迴**勾選框。
* 按一下**確定**按鈕。

## 在 Linux 中停用遞迴
{:#disable-recursion-in-linux}

 * 在作業系統內找出 BIND 配置檔。BIND 配置檔通常位於下列其中一個路徑：
  * /etc/bind/named.conf
  * /etc/named.conf
* 在偏好的編輯器中開啟 named.conf 檔案。
* 將下列詳細資料新增至**選項**區段：<br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* 重新啟動裝置。
