---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary Domains, secondary domain, IBM Cloud DNS servers transfer

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 2 次ドメインについて
{:#about-secondary-domains}

2 次ドメインとは、{{site.data.keyword.BluSoftlayer_notm}} DNS サーバーがご使用のサーバーから権限 DNS サーバー (`ns1.softlayer.com` および `ns2.softlayer.com`) に転送するドメインです。  2 次ドメインをポータルで構成するには、ポータルの**<span style="text-decoration: underline">「パブリック・ネットワーク (Public Network)」</span>**フォルダーで**<span style="text-decoration: underline">「ドメイン・ネーム・システム (Domain Name System)」</span>**をクリックし、**<span style="text-decoration: underline">「2 次 DNS (Secondary DNS)」</span>**リンクをクリックし、最後に**<span style="text-decoration: underline">「2 次 DNS レコードの追加 (Add Secondary DNS Record)」</span>**をクリックしてください。

2 次ドメインをセットアップするには、3 つの情報 (そのドメイン、転送元の*マスター DNS サーバーの IP アドレス*、およびドメインを転送するときの分単位の頻度) が必要になります。<br/>
2 次ドメインが構成されたら、マスター・サーバーの IP アドレスおよび転送間隔を変更できるようになります。  さらに、転送中のドメインを表示し、手動転送を要求し、ご使用の 2 次ドメインを 1 次ドメインに変換し、転送プロセスの間に記録されたエラー・メッセージを調べることもできます。
