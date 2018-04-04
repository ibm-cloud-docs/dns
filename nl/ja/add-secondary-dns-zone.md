---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 2 次 DNS ゾーンの追加

データ損失の対策として 1 次 DNS ゾーンをキャッシングする手段として、{{site.data.keyword.BluSoftlayer_notm}} は 2 次 DNS をすべてのお客様に提供しています。2 次 DNS ゾーンの保守は必須ではありませんが、複数のドメインを持つユーザーには強くお勧めします。2 次 DNS ゾーンを追加するには、以下の手順に従ってください。

* [カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) で、**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。[『「DNS ゾーン (DNS Zones)」画面の使用』](use-dns-zones-screen.html){:new_window}を参照してください。
* **「ゾーンの追加 (Add Zone)」**タブを選択します。
* **「ゾーン (Zone)」**フィールドに**ゾーンのドメイン**を入力します。
* **「マスター・ネーム・サーバー (Master Nameserver)」**フィールドに**マスター・ネーム・サーバーの IP アドレス**を入力します。
* **「転送間隔 (Transfer Interval)」**フィールドに、1 次 DNS ゾーンが 2 次 DNS ゾーンに転送されるときの**転送時間** (分) を入力します。
* そのゾーンを追加するには**「追加 (Add)」**ボタンを、アクションを取り消すには**「キャンセル」**を選択します。

## 次のステップ

2 次 DNS ゾーンを作成した後、そのゾーンは「2 次 DNS ゾーン (Secondary DNS Zones)」画面のゾーンのリストに表示されます。1 次ゾーンから 2 次ゾーンへのデータ転送は、ゾーンの作成時に指定した間隔で行われます。そのゾーンはいつでも[編集](edit-secondary-dns-zone.html)、[手動転送](make-manual-zone-transfer-secondary-dns.html)、または 1 次ゾーンに[変換](convert-secondary-dns-zone-primary-zone.html)できます。また、2 次 DNS ゾーンはいつでも[削除](delete-secondary-dns-zone.html)できます。
