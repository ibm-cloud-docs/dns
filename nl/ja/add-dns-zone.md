---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone, DNS management, Add DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS ゾーンの追加
{:#add-a-dns-zone}

{{site.data.keyword.BluSoftlayer_notm}} による DNS 管理は、{{site.data.keyword.BluSoftlayer_notm}} ネットワーク上にない DNS ゾーンに対しても有効です。 用意されているインターフェースを使用することによって、いつでも DNS ゾーンを 1 つのドメインとして、または一括で追加できます。 DNS ゾーンの追加は現在、[コントロール](https://control.softlayer.com/)・バージョンのカスタマー・ポータルで行われます。 1 つ以上の DNS ゾーンを追加するには、以下の手順に従ってください。

* ユーザー固有の資格情報を使用して、[コントロール](https://control.softlayer.com/)・バージョンのカスタマー・ポータルにログインします。
* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択します
* **「ネットワーク」**ドロップダウン・メニューから**「DNS」**を選択します。
* **「前方ゾーン (Forward Zones)」**を選択します。
* 右上にある**「DNS ゾーンの追加 (Add DNS Zone)」**タブを選択します。
* 1 つのドメインを追加するか、または複数のドメインを追加するかを決定します。<br> <br><table border="1"><tbody><tr><th>追加する対象</th><th>手順</th></tr><tr><td>1 つのドメイン</td><td>画面の<strong>「単一ドメインの追加 (Add single domain)」</strong>セクションで、次の手順を実行します。
<br> <ul><li><strong>「ドメイン・ネーム (Domain Name)」</strong>フィールドに<strong>ドメイン・ネーム</strong>を入力します。</li><li><strong>「IP アドレス (IP Address)」</strong>フィールドに、そのドメイン・ネームが指す <strong>IP アドレス</strong>を入力します。</li><li><strong>「ゾーンの追加 (Add Zone)」</strong>ボタンをクリックして、ドメインを追加します。<br> </li></ul></td></tr><tr><td>複数のドメイン</td><td>ドメインが 1 つの IP アドレスに関連付けられるか、または複数の IP に関連付けられるかを決定します。<br> <p> </p><p> </p><p> </p><p> </p><ul><li>ドメインが 1 つの IP アドレスに関連付けられる場合:<ul><li><strong>「ドメイン (Domains)」</strong>テキスト・ボックスに、<strong>それぞれのドメイン</strong>を入力します。</li><li><strong>「デフォルト IP アドレス (Default IP Address)」</strong>フィールドに、<strong>IP アドレス</strong>を入力します。</li><li><strong>「ゾーンの追加 (Add Zone)」</strong>ボタンをクリックして、ドメインを一括で追加します。</li></ul></li><li>ドメインが複数の IP アドレスに関連付けられる場合:<ul><li><strong>「ドメイン (Domains)」</strong>テキスト・ボックスに、<strong>それぞれのドメイン</strong>と対応する <strong>IP アドレス</strong>を 1 行の項目として入力します。</li><li><strong>「ゾーンの追加 (Add Zone)」</strong>ボタンをクリックして、ドメインを一括で追加します。</li></ul></li><li> </li></ul></td></tr></tbody></table>

## 次のステップ
{:#add-a-dns-zone-next}

DNS ゾーンを追加した後、そのゾーンは、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の[「DNS ゾーン (DNS Zones)」画面](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)で、DNS ゾーンのリストに表示されるようになります。 ゾーンはいつでも[編集](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)または[削除](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone)できます。


