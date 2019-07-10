---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Manual Zone Transfer, DNS Zone transfers, Secondary DNS Zone

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# 2 次 DNS ゾーンの手動ゾーン転送を行う
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

一般に、DNS ゾーン転送は、指定された 2 次 DNS 転送間隔に基づいて自動的に完了します。 手動ゾーン転送を使用すれば、次の自動転送まで待機することなくコンテンツを強制的に転送できます。 手動転送を完了するには、[2 次 DNS ゾーンを設定する必要があります](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone)。 2 次 DNS の手動ゾーン転送を行うには、この記事にある手順に従います。

1. [カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面にナビゲートします。 [『「DNS ゾーン (DNS Zones)」画面の使用』](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window}を参照してください。
2. **「アクション」**ドロップダウン・リストから**「強制転送 (Force Transfer)」**を選択して転送を開始します。

## 次のステップ
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone-next}

転送が開始されると、状況が**「転送中 (Transferring now)」**に変わります。 手動転送を開始後に取り消すことはできません。 データが転送された後、データ転送は、2 次 DNS に対して事前設定されていた転送間隔に戻ります。 頻繁に手動ゾーン転送を行う必要がないように、いつでも[転送間隔を変更できます](/docs/infrastructure/dns?topic=dns-edit-a-secondary-dns-zone)。
