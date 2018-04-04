---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS の概説

インターネットのドメイン・ネーム・システム (DNS) は、サーバーおよびルーターが認識する IP アドレスを、_ドメイン・ネーム_ と呼ばれる分かりやすい名前 (例: `ibm.com`) に変換する方式です。

DNS の概念は単純ですが、ご使用の各種ドメインについてレコードを管理したり保管したりする作業は、便利な方法がなければ非常に単調でつまらない作業となることがあります。

IBM Cloud DNS は、お客様が当社の基本 DNS 管理インターフェースを使用して 1 カ所でドメインを表示したり管理したりできるようにします。また、同一の場所でリバース DNS と 2 次 DNS を管理するオプションも無料で提供されています。

さらに、IBM Cloud は、追加[ネットワーク・ツール](https://console.bluemix.net/docs/infrastructure/network-tools/getting-started.html#getting-started-with-network-tools)も一式提供しています。[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) から当社 DNS インターフェースを使用する方法に関する具体的な説明については、[この資料を参照してください](https://github.ibm.com/Bluemix-Docs/dns/blob/staging/using-the-dns-interface.html)。

## 機能説明
基本レベルでは、{{site.data.keyword.BluSoftlayer_notm}} DNS は、お客様が使用する何らかの DNS 管理ツールと同じように機能します。既存の DNS レコードと対話すること、既存の DNS レコードを編集すること、新規レコードを追加すること、およびリバース DNS に関する情報を更新することが可能です。別の DNS 管理サービスを使用したり自分自身で管理したりするのではなく {{site.data.keyword.BluSoftlayer_notm}} を使用することの主なメリットは、信頼できる中央の場所ですべてのデータを保管することです。

データが失われたりノードで障害が発生したりした場合に備えてユーザーが 1 次 DNS レコードをバックアップできるように、{{site.data.keyword.BluSoftlayer_notm}} は追加サービスとして 2 次 DNS ゾーンを無料でお客様に提供しています。

## DNS の管理方法
多くのユーザーは、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) を使用して 1 次 DNS、リバース DNS、および 2 次 DNS を管理します。このポータルは DNS に関するすべての物事を管理するための当社のポイント・アンド・クリック・インターフェースです。

また、IBM Cloud SoftLayer API (SLAPI) を使用して DNS と対話することもできます。この API の機能は、当社のポータル UI とほとんど同じです。ただし、DNS レコードを一括編集する場合、カスタマー・ポータルで一括処理できるレコードは 20 セットまでですが、API では、これより柔軟な仕様となっています。SLAPI を使用した DNS との対話について詳しくは、[この API 資料](dns-api.html)を参照してください。


