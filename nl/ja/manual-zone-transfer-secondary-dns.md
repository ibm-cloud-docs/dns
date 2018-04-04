---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 2 次 DNS ゾーンの手動ゾーン転送を行う

一般に、DNS ゾーン転送は、指定された 2 次 DNS 転送間隔に基づいて自動的に完了します。手動ゾーン転送を使用すれば、次の自動転送まで待機することなくコンテンツを強制的に転送できます。手動転送を完了するには、[2 次 DNS ゾーンを設定する必要があります](add-secondary-dns-zone.html)。2 次 DNS の手動ゾーン転送を行うには、この記事にある手順に従います。

1. [カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。[『「DNS ゾーン (DNS Zones)」画面の使用』](delete-secondary-dns-record.html){:new_window}を参照してください。
2. **「アクション」**ドロップダウン・リストから**「強制転送 (Force Transfer)」**を選択して転送を開始します。

## 次のステップ

転送が開始されると、状況が**「転送中 (Transferring now)」**に変わります。手動転送を開始後に取り消すことはできません。データが転送された後、データ転送は、2 次 DNS に対して事前設定されていた転送間隔に戻ります。頻繁に手動ゾーン転送を行う必要がないように、いつでも[転送間隔を変更できます](edit-secondary-dns-zone.html)。
