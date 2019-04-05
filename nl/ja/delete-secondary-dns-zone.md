---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 2 次 DNS ゾーンの削除
{:#delete-a-secondary-dns-zone}

2 次 DNS ゾーンを作成した後、そのゾーンをいつでも削除できます。 2 次 DNS ゾーンを削除すると、そのゾーンは検索できなくなることに注意してください。 2 次 DNS レコードを削除するには、以下の手順に従ってください。

 * ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択して、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「セカンダリー・ゾーン」**を選択します。
* 削除が必要なゾーンの**「アクション」**ドロップダウン・リストで**「削除」**を選択します。 ポップアップ確認ボックスが表示されます。
  複数の 2 次ゾーンが存在する場合、表示をフィルタリングして、削除対象のゾーンを見つけることができます。
  {:note}
* 削除するには**「はい (Yes)」**ボタンを、アクションを取り消すには**「いいえ (No)」**ボタンを選択します。

## 次のステップ
{:#delete-a-secondary-dns-zone-next}

2 次 DNS ゾーンが削除されると、1 次ゾーンからの自動転送は停止し、2 次ゾーンは存在しなくなります。 どの時点であっても、2 次 DNS ゾーンが 1 次ゾーンに必要になった場合は、新しい[2 次 DNS ゾーンを作成](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone)することができます。
