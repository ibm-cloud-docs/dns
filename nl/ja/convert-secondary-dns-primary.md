---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 2 次 DNS ゾーンの 1 次ゾーンへの変換

[2 次 DNS ゾーン](add-secondary-dns-zone.html){:new_window}は、いつでも 1 次ゾーンに変換できます。2 次 DNS ゾーンを 1 次ゾーンに変換すると、{{site.data.keyword.BluSoftlayer_notm}} ネーム・サーバーが、変換されたゾーンの権限ネーム・サーバーになります。2 次 DNS ゾーンを 1 次ゾーンに変換するには、以下の手順に従ってください。

* [カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) で、**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。[『「DNS ゾーン (DNS Zones)」画面の使用』](use-dns-zones-screen.html){:new_window}を参照してください。
* 目的の 2 次ゾーンの**「アクション」**ドロップダウン・リストで**「1 次に変換 (Convert to Primary)」**を選択します。
* そのゾーンを変換するには**「はい (Yes)」**ボタンを、アクションを取り消すには**「いいえ (No)」**を選択します。

## 次のステップ

2 次 DNS ゾーンを 1 次ゾーンに変換した後、そのゾーンは**「前方ゾーン (Forward Zones)」**画面に表示されます。以前にそのゾーンに存在していた SOA レコードと NS レコードはすべて、編集できない {{site.data.keyword.BluSoftlayer_notm}} の SOA レコードおよび NS レコードで置き換えられます。その他の[ゾーン・レコードを編集](edit-dns-zone-record.html)することはできます。
