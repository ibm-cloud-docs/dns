---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# cPanel/WHM でのプライベート・ネーム・サーバーの作成

cPanel/WHM 製品を使用すると、いつでもプライベート・ネーム・サーバーを作成できます。プライベート・ネーム・サーバーによって、Web サイトに関連付けられているネーム・サーバー (例えば、`www.yourdomain.com`) が、その Web サイトのネーム・サーバー (例えば、`ns1.yourdomain.com`) を、Web サイトの Web ホストに関連付けられているネーム・サーバー (例えば、`ns1.webhostdomain.com`) の代わりに表示できるようになります。プライベート・ネーム・サーバーをドメインに追加すると、DNS 管理のための追加のオプションが cPanel/WHM で使用できるようにもなります。プライベート・ネーム・サーバーを作成するには、ここに記載されている手順に従ってください。この手順の実行中または実行後に問題が発生した場合は、[チケットをオープン](/general/create-ticket.html)してください。

## ネーム・サーバーに名前を付ける

* ご使用のサーバー (URL は http://xx.xx.xx.xx:2086) で、WHM にログインします。
* **「Server Configuration」**メニューから**「Basic cPanel/WHM Setup」**を選択します。
* 目的のネーム・サーバー・ホスト名を、次の 1 つ以上のフィールドに入力します。
  * Primary Nameserver
  * Secondary Nameserver
  * Tertiary Nameserver
  * Quaternary Nameserver
* **「Save」**ボタンを選択します。

## ドメイン用のゾーン・ファイルの作成

* **「DNS Functions」**メニューから**「Add a DNS Zone」**を選択します。
* ドメインの **IP アドレス**を**「Ip」**フィールドに入力します。
* **ドメイン・ネーム**を**「Domain」**フィールドに入力します。

**注:**また、cPanel の WHM 資料にある[「Create an Account」](http://docs.cpanel.net/twiki/bin/view/AllDocumentation/WHMDocs/CreateAccount)ガイドに従って、ドメイン・アカウントを作成することもできます。

## IP をネーム・サーバーに割り当てる

* **「Network Setup」**メニューから**「Nameserver IPs」**を選択します。
* 最初の**ネーム・サーバー名**を**「Nameserver」**フィールドに入力します。
* **「Assign」**ボタンを選択します。
* ネーム・サーバーごとに、上の手順を繰り返します。

## ネーム・サーバーのセットアップ

* **「Service Configuration」**メニューから**「Nameserver Setup」**を選択します。
* ポップアップ・メッセージにある**「Proceed」**ボタンを選択します。
