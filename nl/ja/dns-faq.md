---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-13"

keywords: DNS servers, fast domain name resolution, DNS FAQ

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}


# DNS FAQ
{:#dns-faq}

## DNS サーバーとは?
{:#what-are-dns-servers}
{: faq}

161.26.0.10 および 161.26.0.11

## ローカル DNS リゾルバーとは?
{:#what-are-local-dns-resolvers}
{: faq}

当社プライベート・ネットワーク上のローカル解決ネーム・サーバーは以下のとおりです。

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

これらのネーム・サーバーでは高速のドメイン・ネーム解決が行われます。これがお客様のパブリック処理能力割り当てを使い尽くすことはありません。 これらのサーバーを使用するには、ご使用のオペレーティング・システムに解決ネーム・サーバーを追加するための正しい手順に従います。

## {{site.data.keyword.BluSoftlayer_notm}} ネーム・サーバー・アドレスとは?
{:#what-are-name-server-addresses}
{: faq}

当社では、権限ネーム・サーバーに 2 つのアドレスを使用していて、解決ネーム・サーバーに 2 つのアドレスを使用しています。

### 権限ネーム・サーバー
{:#authoratative-name-servers}

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### 解決ネーム・サーバー
{:#resolving-name-servers}

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

これらのローカル解決ネーム・サーバーは当社のプライベート・ネットワーク上にあるため、お客様のパブリック処理能力割り当てが使い尽くされることはありません。 

## 自分の 2 次ドメインに対して応答する IBM Cloud DNS サーバーは?
{:#what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}

ご使用の 2 次ドメインに対しては、{{site.data.keyword.BluSoftlayer_notm}} エニーキャスト IPv 対応権限 DNS サーバーが応答します。 このサーバーは以下のアドレスにあります。

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## 自分の 2 次ドメインのゾーン転送に使用される IP アドレスは?
{:#which-ipaddresses-secondary-domain-zone-transfers}
{: faq}

ご使用の 2 次ドメインの転送は、4 つある以下の IP アドレスのいずれかから行われます。

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## パブリック・ネーム・サーバーとプライベート・ネーム・サーバーの違いは?
{:#public-v-private-nameservers}
{: faq}

当社パブリック・ネーム・サーバーは、当社 DNS サーバーにあるドメイン・ネーム用の権限ネーム・サーバーとして機能し、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) を使用して管理されます。 当社パブリック・ネーム・サーバーは、一般的なインターネット利用者のために、、ドメイン・ネームに「応答」し、そのドメイン・ネームを「解決」して IP アドレスにします。

当社解決ネーム・サーバーはプライベート・ネットワーク上にあり、お客様のサーバーの DNS リゾルバーとして機能します。 このプライベート・リゾルバーは、ドメイン・ルックアップのためにインターネットのルート・ネーム・サーバーに問い合わせを行います。 例えば、ご使用のサーバーからメールを送信するには、宛先ドメイン・ネームに対して NSlookup を実行する必要があります。 プライベート DNS サーバーは、プライベート・ネットワーク上でこの情報を解決することにより、お客様の帯域幅使用量を抑え続け、権限サーバーに対する負荷を軽減し、素早い解決を提供します。 プライベート・ネットワーク・リゾルバーは、お客様向けの便利なサービスです。

## 自分がネーム・サーバーに対して実行できることは?
{:#what-are-my-name-server-options-faq}
{: faq}

ベア・メタル・サーバーがある場合、ネーム・サーバーに関する代表的な選択肢として以下の 4 つがあります。

* ドメイン・ネーム・レジストラーのネーム・サーバーを使用してドメイン・ネームを管理します。
* {{site.data.keyword.BluSoftlayer_notm}} ネーム・サーバーを使用してドメイン・ネームを管理します。
* サード・パーティーの DNS サービスを使用してドメイン・ネームを管理します。
* ご使用のサーバー上で自前のネーム・サーバーを稼働させてドメイン・ネームを管理します。

最初の 3 つの選択肢に関しては、サード・パーティーのネーム・サーバー (例: `ns1.softlayer.com` および `ns2.softlayer.com`) を使用します。 最後の選択肢に関しては、お客様のドメインをネーム・サーバーとして使用します (例: `ns1.yourdomain.com` および `ns2.yourdomain.com`)。この場合は、ご使用のサーバー上で DNS サービスを実行する必要があります。 また、ご使用のドメインをネーム・サーバーとしてレジストラーに登録する必要もあります。 ネーム・サーバー登録は通常は無料ですが、基本的なドメイン・ネーム登録プロセス以外の追加ステップが必要です。

当社のお客様には、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) を使用して完全に管理される無料の DNS サービスが提供されます。 当社では、お客様の DNS およびネーム・サーバーを {{site.data.keyword.BluSoftlayer_notm}} で管理できるようにすることを強くお勧めします。その理由は、当社冗長システムが使用されていて、管理が容易であり、DNS 関連の問題を素早くトラブルシューティングできるためです。

## 自分で自分のリバース DNS をセットアップする方法とは?
{:#how-do-i-setup-reverse-dns}
{: faq}

リバース DNS は、[カスタマー・ポータル![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) を使用してセットアップします。リバース DNS をセットアップする方法については、 [『リバース DNS レコードの更新』](/docs/infrastructure/dns?topic=dns-update-reverse-dns-record)を参照してください。


## DNS の変更が伝搬するまでの時間は?
{:#how-long-for-dns-changes-propagate}
{: faq}

DNS の変更が伝搬するまでの時間は、DNS レコードの存続時間 (TTL) 設定によって異なります。

デフォルト TTL は 1 日です。つまり、ドメイン・ネームの変更がインターネット全体に伝搬するまで 1 日かかります。 変更を頻繁に行う予定の場合は TTL を短縮できますが、TTL が短くなると、ネーム・サーバーに対する負荷が大きくなります。 負荷が大きくなると、エンド・ユーザーに対する応答時間が長くなり、エンド・ユーザーの全体的な満足度に影響する可能性があります。

TTL の設定値を大きくすると、ローカル ISP キャッシングが行われるため、DNS のパフォーマンスは向上します。 TTL の設定値を小さくすると、名前解決が増えるため、DNS のパフォーマンスは低下します。

TTL を検証するには、ドメインの Start of Authority (SOA) レコードを確認します。 ドメイン情報を確認するための優れたツールが [CentralOps.net ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://centralops.net/co/) で提供されています

TTL は秒単位でリストされます。TTL を分単位に変換するには TTL を 60 で除算します。TTL を時間単位に変換するには TTL を 3600 で除算します。


## ドメイン転送後に、そのドメインと変更内容が表示されるまでにかかる時間は?
{:#how-long-transfer-change-visiblity}
{: faq}

ドメインとそのドメインに対する変更のいずれかまたは両方は、転送完了直後に IBM Cloud DNS サーバーに表示されます。 DNS の伝搬の性質上、変更が他の DNS サーバーで表示されるまで時間がかかります。

## プライベート・ネットワーク上で AXFR 要求を完了できますか?
{:#axfr-request-private-network}
{: faq}

現在、{{site.data.keyword.BluSoftlayer_notm}} はプライベート・ネットワーク上の AXFR 要求をサポートしていません。 AXFR 要求はすべてパブリック・ネットワーク上で完了する必要があります。
