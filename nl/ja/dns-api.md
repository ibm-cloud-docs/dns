---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS API の概要

ユーザーは `SoftLayer_Dns_Domain` サービスを使用して {{site.data.keyword.BluSoftlayer_notm}} 権限 DNS サーバーと対話できます。 

各 `SoftLayer_Dns_Domain` には、`resourceRecords` リレーショナル・プロパティーによって参照される `SoftLayer_DNS_Domain_ResourceRecords` の集合があります。`SoftLayer_Dns_Domain` サービスを使用してリソース・レコードと対話することは可能ですが、最初にゾーンを作成した直後は `SoftLayer_Dns_Domain_ResourceRecord` サービスを使用することが最適です。

## ドメイン
### リスト
{{site.data.keyword.BluSoftlayer_notm}} ネーム・サーバーで現在ホストされているすべてのドメインのリストを、`SoftLayer_Account::getDomains` を使用して取得できます。これにより、`SoftLayer_Dns_Domain` テンプレート・オブジェクトの配列が返されます。この呼び出しを拡張すれば、オブジェクト・マスクを使用して、これらのドメインに関連付けられたレコードをプルすることもできます。

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### 作成
新規ゾーンを作成するには、`SoftLayer_Dns_Domain` テンプレート・オブジェクトを作成して `SoftLayer_Dns_Domain::createObject` に渡す必要があります。作成時に、`ns1.softlayer.com` および `ns2.softlayer.com` 用の NS レコードが自動的に追加されます。正常に作成するには、テンプレート・オブジェクトに少なくとも 1 つの A レコードまたは AAAA レコードを組み込みますドメインのシリアル番号は API によって追加または更新されるため、テンプレート・オブジェクトに組み込む必要はありません。

`SoftLayer_Dns_Domain` オブジェクトを作成するときは、以下のプロパティーが必要です。
 * name - TLD の「example.com」を含むドメイン・ネーム
 * resourceRecords - 少なくとも 1 つの SoftLayer_Dns_Domain_ResourceRecord を含む配列
 
```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', null, $apiUser, $apiKey);
$template = new stdClass();
$template->name = "createexample.com";
$template->resourceRecords = array();
$template->resourceRecords[0] = new stdClass();
$template->resourceRecords[0]->data = '127.0.0.1';
$template->resourceRecords[0]->host = 'server1';
$template->resourceRecords[0]->type = 'a';
$result = $client->createObject($template);
print_r($result);
```

`SoftLayer_Dns_Domain:: createObject` は、データが完全に設定された `SoftLayer_Dns_Domain` オブジェクトを返します。

### 編集
既存の `SoftLayer_Dns_Domain` エントリーは変更できません。ゾーン名に対する変更をリファクタリングして新規ゾーンを作成することが必要となります。

### 削除
ゾーンを削除するには、`SoftLayer_Dns_Domain::deleteObject` を使用します。この方法では、初期設定パラメーターのみを指定する必要があります。

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` はブール値を返します。成功の場合は `true` が返され、失敗の場合は `false` が返されます。

## レコード
### リスト
上記の方法のほか、`SoftLayer_Dns_Domain::getResourceRecords` を使用してドメイン・リソース・レコードを取得できます。この場合は、`SoftLayer_Dns_DomainResourceRecord` オブジェクトの配列が返されます。

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### 作成
`SoftLayer_Dns_Domain_ResourceRecord` サービスを使用してレコードを直接作成するには、`SoftLayer_Dns_Domain_ResourceRecord` テンプレート・オブジェクトを作成して `SoftLayer_Dns_Domain_ResourceRecord::createObject` に渡します。host プロパティーで使用する「@」はワイルドカード・ホスト名を示します。

{{site.data.keyword.BluSoftlayer_notm}} DNS システムは以下のレコード・タイプをサポートします。
 * a
 * aaaa
 * cname
 * mx
 * ns
 * ptr
 * soa
 * spf
 * srv
 * txt

テンプレート・オブジェクトには、少なくとも以下の項目が含まれていなければなりません。
 * data - レコードの値
 * host - ゾーンの下に追加されるラベル
  
```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', null, $apiUser, $apiKey);
$domainId = 123456;
 
$template = new stdClass();
$template->data = 'webserver01.example.com';
$template->host = 'www';
$template->type = 'cname';
$template->domainId = $domainId;
 
$result = $client->createObject($template);
print_r($result);

```

### 編集
リソース・レコードを編集するには、テンプレート・オブジェクトを `SoftLayer_Dns_Domain_ResourceRecord::editObject` に渡します。テンプレート・オブジェクトには、以下の項目が含まれていなければなりません。

 * id - 編集対象の `SoftLayer_Dns_Domain_ResourceRecord` の ID
 * domainId - `SoftLayer_Dns_Domain` (当該リソース・レコードはこれの子レコードである) の ID
 * 変更対象のプロパティー [注: ドメインのシリアル番号は API によって自動的に更新されます。]
  
```
$domainId = 45567;
$resourceRecordId = 1234;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $resourceRecordId, $apiUser, $apiKey);
 
$template = new stdClass();
$template->id = $resourceRecordId;
$template->domainId = $domainId;
$template->data = '127.0.0.1';
$template->host = 'server01';
 
$result = $client->editObject($template);
print_r($result);
```
また、初期設定パラメーターにリソース・レコード ID プロパティーを取り込むことも必要となります。`SoftLayer_Dns_Domain_ResourceRecord:: editObject` によってブール値が返されます。

### 削除
レコードを削除するには、`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` を使用します。この方法では、初期設定パラメーターのみを指定する必要があります。

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` はブール値を返します。成功の場合は `true` が返され、失敗の場合は `false` が返されます。
