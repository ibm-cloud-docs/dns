---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 2 次 DNS ゾーンの 1 次ゾーンへの変換
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

[2 次 DNS ゾーン](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window}は、いつでも 1 次ゾーンに変換できます。 2 次 DNS ゾーンを 1 次ゾーンに変換すると、{{site.data.keyword.BluSoftlayer_notm}} ネーム・サーバーが、変換されたゾーンの権限ネーム・サーバーになります。 2 次 DNS ゾーンを 1 次ゾーンに変換するには、以下の手順に従ってください。

* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択して、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「セカンダリー・ゾーン」**を選択します。
* 目的の 2 次ゾーンの**「アクション」**ドロップダウン・リストで**「1 次に変換 (Convert to Primary)」**を選択します。
* そのゾーンを変換するには**「はい (Yes)」**ボタンを、アクションを取り消すには**「いいえ (No)」**を選択します。

## 次のステップ
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

2 次 DNS ゾーンを 1 次ゾーンに変換した後、そのゾーンは**「前方ゾーン (Forward Zones)」**画面に表示されます。 以前にそのゾーンに存在していた SOA レコードと NS レコードはすべて、編集できない {{site.data.keyword.BluSoftlayer_notm}} の SOA レコードおよび NS レコードで置き換えられます。 その他の[ゾーン・レコードを編集](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)することはできます。
