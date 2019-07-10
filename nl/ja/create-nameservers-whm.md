---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: create your own nameservers, cPanel, WHM

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# cPanel/WHM での独自のネーム・サーバーの作成
{:#create-your-own-nameservers-in-cpanel-whm}

ここでは、Web Host Manager (WHM) を使用して独自のネーム・サーバーを作成するときの手順について説明します。 これらの手順を終えた後で問題が発生した場合、この記事を参照するサポート・チケットを送信してください。

1. まず、ネーム・サーバーの名前を決定します。 例えば、ホスティング会社の名前が「Awesome Server Hosting」であるため、`ns1.awesomeserverhosting.com` と `ns2.awesomeserverhosting.com` をセットアップするとします。

* ご使用のブラウザーで `https://XX.XX.XX.XX:2087` を開いて、サーバー上の WHM にログインします。

* ネーム・サーバーをセットアップするには、左側のバーで最初のオプション「Basic cPanel/WHM Setup」を選択します。 

 * ここで、1 次/2 次/3 次/4 次ネーム・サーバーの名前を設定できます。

 * 完了したら、「Save」ボタンを選択します。

2. 次に、サーバーに `awesomeserverhosting.com` のゾーン・ファイルを作成します。 この作業を行うには、以下の 2 つの方法があります。

1 番目の方法: 「awesomeserverhosting.com」のドメイン・アカウントを作成します。 これについての説明は、この記事の内容の範囲外です。詳しくは、[cPanel 資料](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)を参照してください。 

   * 左側のサイドバーで、「DNS Functions」の下の「Add a DNS Zone」を選択します。

   * メイン Web サイトが `awesomeserverhosting.com` 用にホストされている IP アドレスと、当然ながらドメイン・ネームも指定します。

   **注: これは、このサーバー上で `awesomeserverhosting.com` をホスティングする予定ではない場合のみ実行してください。**

   * 見出し**「Networking Setup」**の下で、**「Nameserver IPs」**をクリックします。

   * ご使用のネーム・サーバーの名前を指定します。 例えば、`ns1.awesomeserverhosting.com` を送信し、さらに `ns2.awesomeserverhosting.com` を送信してください。

   * 左側のバーで、**「Service Configuration」**の下の**「Nameserver Setup」**を見つけます。

   * 次のようなメッセージが表示されます。「We recommend you do not enable the nameserver unless you are going to use it. If you wish to disable the nameserver you can always turn it off in the Service Manager」。

   * ネーム・サーバーが稼働状態になりました。**「Proceed >>」**のマークが付けられているボタンを選択してください。 `cPanel` ツールによって、ご使用のサーバーに適切なパッケージがインストールされ、ご使用のドメイン・ネーム・サービスをホストするためにそれらのパッケージが正しく動作するように構成されます。 これですべて設定されました。

外部リンク

* [cPanel 資料](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
