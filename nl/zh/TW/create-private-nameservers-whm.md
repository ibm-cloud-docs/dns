---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Select Basic cPanel, Private Nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 在 cPanel/WHM 中建立專用名稱伺服器
{:#create-private-nameservers-in-cpanel-whm}

使用 cPanel/WHM 產品，您可以隨時建立專用名稱伺服器。專用名稱伺服器容許與網站（例如，`www.yourdomain.com`）相關聯的名稱伺服器，來顯示網站的名稱伺服器（例如，`ns1.yourdomain.com`），而不是顯示與網站的 Web 主機相關聯的名稱伺服器（例如，`ns1.webhostdomain.com`）。將專用名稱伺服器新增至網域也會開啟 cPanel/WHM 內關於 DNS 管理的其他選項。請遵循本文章中的步驟，以建立專用名稱伺服器。如果在執行此程序期間或之後發生問題，請[開立問題單](/docs/get-support?topic=get-support-getting-customer-support)。

## 將名稱伺服器命名
{:#name-the-nameserver}

* 在伺服器上登入 WHM，其 URL 為：`http://xx.xx.xx.xx:2086`。
* 從**伺服器配置**功能表中，選取**基本 cPanel/WHM 設定**。
* 在下列一個以上的欄位中，輸入想要的名稱伺服器主機名稱：
  * 主要名稱伺服器
  * 次要名稱伺服器
  * 第三層名稱伺服器
  * 第四層名稱伺服器
* 選取**儲存**按鈕。

## 建立網域的區域檔案
{:#create-a-zone-file-for-the-domain}

* 從 **DNS 功能**功能表中，選取**新增 DNS 區域**。
* 在 **Ip** 欄位中輸入網域的 **IP 位址**。
* 在**網域**欄位中輸入**網域名稱**。

或者，您可以利用 cPanel 的 WHM 文件中的[建立帳戶](https://docs.cpanel.net/display/70Docs/Create+a+New+Account)手冊來建立「網域帳戶」。
{:note}

## 將 IP 指派給名稱伺服器
{:#assign-an-ip-to-the-nameserver}

* 從**網路設定**功能表中，選取**名稱伺服器 IP**。
* 請在**名稱伺服器**欄位中輸入第一個**名稱伺服器名稱**。
* 選取**指派**按鈕。
* 針對每一個名稱伺服器，重複上述步驟。

## 設定名稱伺服器
{:#setup-the-nameserver}

* 從**服務配置**功能表中選取**名稱伺服器設定**。
* 選取蹦現訊息上的**繼續**按鈕。
