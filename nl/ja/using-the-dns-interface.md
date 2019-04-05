---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS インターフェースの使用法
{:#how-to-use-the-dns-interface}

IBM Cloud カスタマー・ポータルで DNS インターフェースを使用するには、以下の手順に従ってください。

* [カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) にナビゲートします。
* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択します
* **「ネットワーク」->「DNS」->「前方ゾーン (Forward Zones)」**を選択します。
* 管理するドメインを選択するか、またはページの右側にある**「DNS ゾーンの追加 (Add DNS Zone)」**ボタンを選択します。

## DNS インターフェースの概説
{:#dns-interface-overview}
カスタマー・ポータルにある DNS インターフェースを操作することによって、ご使用の DNS におけるすべての側面を管理するためのすべての機能が得られます。 インターフェースのどの画面でも、その画面の上部にある静的メニュー・バーによって、すべてのタイプの DNS 管理を実行できます。

## DNS の管理
{:#manage-dns}
ポータルにある DNS インターフェースに到達すると、すぐに**「DNS の管理 (Manage DNS)」**画面が表示されます。この画面では、ご使用のアカウントに関連付けられている既存の 1 次 DNS を表示、編集、または削除できます。

* 新規レコードを追加するには、**「新規レコードの追加 (Add New Record)」** の下にあるフィールドに入力し、**「レコードの追加 (Add Record)」**ボタンをクリックするだけです。
* 既存のレコードを変更するには、そのレコードが入っている行をクリックしてください。そのレコードは**編集**モードに変わります。 設定を目的の値に変更して、**「更新」**をクリックします。
* レコードを削除するには、そのレコードの右側にある赤い円を選択し、プロンプトに対して**「はい (Yes)」**をクリックします。

## 2 次 DNS
{:#secondary-dns}

* [カスタマー・ポータルのクラシック・インフラストラクチャー ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) にナビゲートします。
* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択します
* **「ネットワーク」->「DNS」->「2 次ゾーン (Secondary Zones)」**を選択します。

この画面で、2 次 DNS 設定を追加または変更できます。

* 新規レコードを追加するには、**「ゾーンの追加 (Add Zone)」**を選択し、フィールドに入力して**「追加」**を選択します。
* 2 次 DNS レコードを削除するか、または 1 次レコードに変換するには、ページの右上にある**「アクション」**ドロップダウンから該当するオプションを選択します。

## リバース DNS
{:#reverse-dns}

ポータル・ナビゲーションで DNS インターフェースを使用するには、以下の手順に従ってください。

* [カスタマー・ポータルのクラシック・インフラストラクチャー ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) にナビゲートします。
* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択します
* **「ネットワーク」->DNS->「レコードの逆引き (Reverse Records)」**を選択します。
* ドロップダウン・メニューで、リバース DNS を変更する対象の IP アドレスを選択または入力して、**「IP の表示 (View IP)**を選択します。
  * レコードを追加するには、リバース DNS エントリーに使用するホスト名を入力します。
  * そのレコードの TTL (存続時間) を設定します。
  * 情報を確認したら、**「保存」**を選択します。

ページの右側にある**「このサブネット内のすべての IP の RDNS を編集 (Edit RDNS for all IPs in this Subnet)」**をクリックすると、サブネット全体を編集できます。

* このページで、更新する IP の行を選択します。
* 情報をフィールドに入力してから、**「更新」**を選択します。 「メモ」フィールドはオプションです。

<!--## Propagation Check

* Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network > Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
