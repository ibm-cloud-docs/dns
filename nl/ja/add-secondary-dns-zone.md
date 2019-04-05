---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, IBM Cloud, Add Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 2 次 DNS ゾーンの追加
{:#add-a-secondary-dns-zone}

データ損失の対策として 1 次 DNS ゾーンをキャッシングする手段として、{{site.data.keyword.BluSoftlayer_notm}} は 2 次 DNS をすべてのお客様に提供しています。 2 次 DNS ゾーンの保守は必須ではありませんが、複数のドメインを持つユーザーには強くお勧めします。 2 次 DNS ゾーンを追加するには、以下の手順に従ってください。

* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択して、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「セカンダリー・ゾーン」**を選択します。
* **「ゾーンの追加 (Add Zone)」**タブを選択します。
* **「ゾーン (Zone)」**フィールドに**ゾーンのドメイン**を入力します。
* **「マスター・ネーム・サーバー (Master Nameserver)」**フィールドに**マスター・ネーム・サーバーの IP アドレス**を入力します。
* **「転送間隔 (Transfer Interval)」**フィールドに、1 次 DNS ゾーンが 2 次 DNS ゾーンに転送されるときの**転送時間** (分) を入力します。
* そのゾーンを追加するには**「追加 (Add)」**ボタンを、アクションを取り消すには**「キャンセル」**を選択します。

## 次のステップ
{:#add-a-secondary-dns-zone-next}

2 次 DNS ゾーンを作成した後、そのゾーンは「2 次 DNS ゾーン (Secondary DNS Zones)」画面のゾーンのリストに表示されます。 1 次ゾーンから 2 次ゾーンへのデータ転送は、ゾーンの作成時に指定した間隔で行われます。 そのゾーンはいつでも[編集](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)、[手動転送](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone)、または 1 次ゾーンに[変換](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone)できます。 また、2 次 DNS ゾーンはいつでも[削除](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone)できます。
