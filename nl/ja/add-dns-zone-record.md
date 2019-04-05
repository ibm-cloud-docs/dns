---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone Record, TTL Select, Relative Weight

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS ゾーン・レコードの追加
{:#add-a-dns-zone-record}

[DNS ゾーンを追加](/docs/infrastructure/dns?topic=dns-add-a-dns-zone)した後、いつでもレコードをそのゾーンに追加できます。 以下のレコードがあります。

* A (ホスト) レコード
* AAAA (ホスト) レコード
* CNAME (別名) レコード
* MX (Mail Exchange) レコード
* TXT (テキスト) レコード
* SRV (サービス) レコード

DNS ゾーン・レコードを追加するには、以下の手順に従ってください。

* 目的の**「DNS ゾーン (DNS Zone)」**画面にナビゲートします。 [『「DNS ゾーン (DNS Zones)」画面の使用』](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)を参照してください。
* レコードが追加される先の DNS ゾーンを選択します。
* **「リソース・タイプ」**ドロップダウン・リストから、目的の**リソース・タイプ**を選択します。
* 新規レコードの残りのフィールドに入力します。 詳しくは、下の表を参照してください。<br/><br/><table border="1"><tbody><tr><th scope="col">レコード・タイプ</th><th scope="col">フィールド</th><th scope="col">項目</th></tr><tr><td rowspan="3">A (ホスト)、AAAA (ホスト)、CNAME (別名)</td><td>ホスト</td><td><strong>ホスト名</strong>を入力します。</td></tr><tr><td>指す対象 (Points To)</td><td>ホスト・レコードが指す <strong>IP アドレス</strong>を入力します。</td></tr><tr><td>TTL</td><td>ドロップダウン・リストから存続時間 (TTL) を選択します。 TTL はデフォルトで 15 分です。</td></tr><tr><td rowspan="4">MX (Mail Exchange)</td><td>優先順位 (Priority)</td><td>ターゲット・ホストの<strong>優先順位</strong>を入力します。 数値が小さいほど優先順位は高くなります。</td></tr><tr><td>ホスト</td><td><strong>ホスト名</strong>を入力します。</td></tr><tr><td>進む (Goes)</td><td>メール・サーバーの <strong>CNAME</strong> を入力します。 これは通常、mail.example.com と表示されます。</td></tr><tr><td>TTL</td><td>ドロップダウン・リストから存続時間 (TTL) を選択します。 TTL はデフォルトで 15 分です。</td></tr><tr><td rowspan="3">TXT (テキスト)</td><td>名前</td><td><strong>@</strong> または<strong>ドメイン・ネーム</strong>を入力します。</td></tr><tr><td>値</td><td>ドメインまたは IP の適切な E メール終了権限を検証するための<strong>レコード</strong>を入力します。</td></tr><tr><td>TTL</td><td>ドロップダウン・リストから存続時間 (TTL) を選択します。 TTL はデフォルトで 15 分です。</td></tr><tr><td rowspan="8">SRV (サービス・レコード)</td><td>サービス</td><td>目的のサービスの<strong>シンボル名</strong>を入力します。</td></tr><tr><td>プロトコル</td><td>ドロップダウン・リストから、使用する<strong>プロトコル</strong>を選択します。</td></tr><tr><td>優先順位 (Priority)</td><td>ターゲット・ホストの<strong>優先順位</strong>を入力します。 数値が小さいほど優先順位は高くなります。</td></tr><tr><td>重みづけ</td><td>同じ優先度を持つレコードの<strong>相対的な重み</strong>を入力します。</td></tr><tr><td>ポート</td><td>サービスを検出する対象の <strong>TCP または UPD ポート</strong>を入力します。</td></tr><tr><td>ホスト (オプション)</td><td>サービスの<strong>ホスト名</strong>を入力します。</td></tr><tr><td>ターゲット (Target)</td><td>サービスを提供するマシンの<strong>正規ホスト名</strong>を入力します。</td></tr><tr><td>TTL</td><td>ドロップダウン・リストから存続時間 (TTL) を選択します。 TTL はデフォルトで 15 分です。</td></tr></tbody></table><br/>
* **「レコードの追加 (Add Record)」**ボタンを選択して、新規ゾーン・レコードを追加します。

## 次のステップ
{:#add-a-dns-zone-record-next}

ゾーン・レコードを追加した後、そのレコードは、この画面の**「既存のレコード (Existing Record)」**セクションに表示されるようになります。 ゾーン・レコードはいつでも[編集](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)または[削除](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone)できます。
