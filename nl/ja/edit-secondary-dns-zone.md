---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Master Nameserver

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 2 次 DNS ゾーンの編集
{:#edit-a-secondary-dns-zone}

2 次 DNS ゾーンは、マスター・ネーム・サーバーや転送間隔を更新するためにいつでも編集できます。 2 次 DNS ゾーンを編集するには、以下の手順に従います。

* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択して、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「セカンダリー・ゾーン」**を選択します。
* ゾーンを編集のために開くには、**2 次 DNS ゾーンを含む行**で任意の場所をクリックします。
  複数の 2 次ゾーンが存在する場合、表示をフィルタリングして、編集が必要なゾーンを見つけることができます。
  {:note}  
* 必要に応じて**「マスター・ネーム・サーバー (Master Nameserver)」**フィールドと**「転送間隔 (Transfer Interval)」**フィールドを更新します。
* **「更新」**ボタンを選択して 2 次 DNS ゾーンを更新するか、または**「キャンセル」**を選択してアクションを取り消します。

## 次のステップ
{:#edit-a-secondary-dns-zone-next}

2 次 DNS ゾーンの編集後、**「マスター・ネーム・サーバー (Master Nameserver)」**と**「転送間隔 (Transfer Interval)」**の値は更新を反映し、2 次ゾーンは新しい情報に基づいて転送を受信し始めます。 上記の手順を繰り返すことで、ゾーンはいつでも編集できます。
