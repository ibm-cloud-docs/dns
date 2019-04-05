---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Terminology, Caching, individual DNS servers, DNS resolver

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS 用語
{:#dns-terminology}

## キャッシングと存続時間
{:#caching-and-time-to-live}

DNS のようなシステムでは大量の要求が生成されるため、設計者は個々の DNS サーバーの負荷を軽減する以下のようなメカニズムを提供しています。

DNS リゾルバー (つまりクライアント) は DNS 応答を受け取ると、その応答を一定の期間 (存続時間 (TTL) と呼ばれる)、キャッシングします。 TTL の値は、応答を渡す DNS サーバーの管理者によって設定されます。 応答がキャッシングされると、リゾルバーはキャッシングされた (保管された) 応答を調べます。TTL が過ぎたとき (または、管理者が手動でリゾルバーのメモリーから応答をフラッシュしたとき) に限り、リゾルバーは同じ情報について DNS サーバーに問い合わせを行います。

## Start of Authority (SOA) レコード・パラメーター
{:#soa-record-parameters}

通常、存続時間は Start of Authority (SOA) レコードに指定されます。 SOA パラメーターは以下のとおりです。

### シリアル
{:#soa-record-parameters-serial}

当該ゾーン・ファイルの改訂回数。 ゾーン・ファイルが変更されるたびにこの数を増やして、変更がすべての 2 次 DNS サーバーに配布されるようにします。

### 更新
{:#soa-record-parameters-refresh}

ドメインの 1 次ネーム・サーバーから得られる DNS ゾーンの新規コピーを検査するために 2 次ネーム・サーバーが待機しなければならない時間 (秒)。 ゾーン・ファイルが変更されている場合、2 次 DNS サーバーは、1 次 DNS サーバーのゾーンに一致するようにゾーンのコピーを更新します。

### 再試行
{:#soa-record-parameters-retry}

2 次ネーム・サーバーでの更新の試みが失敗した場合に、ドメインの 1 次ネーム・サーバーが、その 2 次ネーム・サーバーを含むドメインのゾーンを再び更新しようとする前に待機しなければならない時間 (秒)。

### 期限切れ
{:#soa-record-parameters-expire}

2 次ネーム・サーバーがゾーンを保持する時間 (秒)。この時間が過ぎると、2 次ネーム・サーバーは権限サーバーとみなされなくなります。

### 最小
{:#soa-record-parameters-minimum}

ドメインのリソース・レコードが有効である時間 (秒)。 これは最小 TTL とも呼ばれ、個々のリソース・レコードの TTL でオーバーライドできます。

### TTL (存続時間)
{:#soa-record-parameters-ttl}

ドメイン・ネームがローカルにキャッシングされている時間 (秒)。この時間が過ぎると、更新情報がないかを確認するためにドメイン・ネームは権限ネーム・サーバーに返されます。
