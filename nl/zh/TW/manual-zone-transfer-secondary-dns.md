---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 進行次要 DNS 區域的手動區域傳送

一般而言，會根據您指定的次要 DNS 傳送間隔，自動完成「DNS 區域」傳送。您可以使用「手動區域傳送」來強制傳送內容，否則，要等到下一個自動傳送時才進行傳送。若要完成手動傳送，[必須建立次要 DNS 區域](add-secondary-dns-zone.html)。遵循本文章中的步驟，為次要 DNS 進行手動區域傳送。

1. 導覽至[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/) 中的**次要 DNS 區域**畫面。請參閱[使用 DNS 區域畫面](delete-secondary-dns-record.html){:new_window}。
2. 從**動作**下拉清單中選取**強制傳送**，以開始傳送。

## 後續情形

傳送開始之後，狀態會變更為**立即傳送**。手動傳送在開始之後就不能取消。傳送資料之後，資料傳送將回到先前為「次要 DNS」設定的傳送間隔。可隨時[變更傳送間隔](edit-secondary-dns-zone.html)，以避免需要經常進行手動區域傳送。
