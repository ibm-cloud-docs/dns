---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 2 次 DNS ゾーンの編集

2 次 DNS ゾーンは、マスター・ネーム・サーバーや転送間隔を更新するためにいつでも編集できます。2 次 DNS ゾーンを編集するには、以下の手順に従います。

* [カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) で**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。[『「DNS ゾーン (DNS Zones)」画面の使用』](delete-secondary-dns-record.html){:new_window}を参照してください。
* ゾーンを編集のために開くには、**2 次 DNS ゾーンを含む行** で任意の場所をクリックします。
  * **注:** 複数の 2 次ゾーンが存在する場合に、編集が必要とされるゾーンを見つけるには、ビューをフィルター操作します。
* 必要に応じて**「マスター・ネーム・サーバー (Master Nameserver)」**フィールドと**「転送間隔 (Transfer Interval)」**フィールドを更新します。
* **「更新」**ボタンを選択して 2 次 DNS ゾーンを更新するか、または**「キャンセル」**を選択してアクションを取り消します。

## 次のステップ

2 次 DNS ゾーンの編集後、**「マスター・ネーム・サーバー (Master Nameserver)」**と**「転送間隔 (Transfer Interval)」**の値は更新を反映し、2 次ゾーンは新しい情報に基づいて転送を受信し始めます。上記の手順を繰り返すことで、ゾーンはいつでも編集できます。
