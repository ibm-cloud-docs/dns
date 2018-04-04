---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 開始使用 DNS API。

使用者可以透過 `SoftLayer_Dns_Domain` 服務，與 {{site.data.keyword.BluSoftlayer_notm}} 主 DNS 伺服器互動。 

每一個 `SoftLayer_Dns_Domain` 都有 `resourceRecords` 關聯式內容所參照的 `SoftLayer_DNS_Domain_ResourceRecords` 的集合。可以透過 `SoftLayer_Dns_Domain` 服務與資源記錄互動；不過，最好在建立起始區域之後，直接使用 `SoftLayer_Dns_Domain_ResourceRecord` 服務。

## 網域
### 清單
{{site.data.keyword.BluSoftlayer_notm}} 名稱伺服器上目前管理的所有網域之清單，您可以使用 `SoftLayer_Account::getDomains` 來擷取它，該指令會傳回 `SoftLayer_Dns_Domain` 範本物件的陣列。您也可以使用物件遮罩來延伸此呼叫，以取回與這些網域相關聯的記錄。

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### 建立
若要建立新的區域，必須建立 `SoftLayer_Dns_Domain` 範本物件，並傳遞至 `SoftLayer_Dns_Domain::createObject`。在建立期間，會自動新增 `ns1.softlayer.com` 和 `ns2.softlayer.com` 的 NS 記錄。範本物件至少要包含一個 A 或 AAAA 記錄，才能順利建立。
API 會新增或更新網域序號，因此不需要將它們併入範本物件中。

建立 `SoftLayer_Dns_Domain` 物件時，需要下列內容。
 * name - 包含 TDL "example.com" 的網域名稱
 * resourceRecords - 至少有一個 SoftLayer_Dns_Domain_ResourceRecord 的陣列
 
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

`SoftLayer_Dns_Domain::createObject` 會傳回完整移入的 `SoftLayer_Dns_Domain` 物件。

### 編輯
無法修改現有的 `SoftLayer_Dns_Domain` 項目。區域名稱的變更應經過重構，才能建立新區域。

### 刪除
區域的移除是使用 `SoftLayer_Dns_Domain::deleteObject` 來完成。此方法只需要提供一個 init 參數。

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` 會傳回布林值：`true` 代表成功，`false` 代表失敗。

## 記錄
### 清單
除了上述方法之外，還可以使用 `SoftLayer_Dns_Domain::getResourceRecords` 來擷取網域資源記錄，其將傳回 `SoftLayer_Dns_DomainResourceRecord` 物件的陣列。

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### 建立
直接透過 `SoftLayer_Dns_Domain_ResourceRecord` 服務建立記錄，是透過建立 `SoftLayer_Dns_Domain_ResourceRecord` 範本物件及將它傳遞至 `SoftLayer_Dns_Domain_ResourceRecord::createObject` 來完成。在主機內容中使用 '@' 表示是一個萬用字元主機名稱。

{{site.data.keyword.BluSoftlayer_notm}} DNS 系統支援這些記錄類型：
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

範本物件必須至少包含：
 * data - 記錄的值
 * host - 要新增至區域下的標籤
  
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

### 編輯
透過將範本物件傳遞至 `SoftLayer_Dns_Domain_ResourceRecord::editObject`，以編輯資源記錄。範本物件必須包含：

 * id - 要編輯的 `SoftLayer_Dns_Domain_ResourceRecord` 的 ID。
 * domainId - 此資源記錄為其子記錄的 `SoftLayer_Dns_Domain` 的 ID
 * 要變更的內容 [附註：網域序號由 API 自動更新。]
  
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
也必須在 init 參數中移入資源記錄 ID 內容。`SoftLayer_Dns_Domain_ResourceRecord::editObject` 傳回布林值

### 刪除
記錄的移除是使用 `SoftLayer_Dns_Domain_ResourceRecord::deleteObject` 來完成。此方法只需要提供一個 init 參數。

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` 會傳回布林值：`true` 代表成功，`false` 代表失敗。
