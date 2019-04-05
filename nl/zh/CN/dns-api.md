---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Domain service, DNS API, resource records

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS API 入门￼
{:#getting-started-with-the-dns-api}

用户可以通过 `SoftLayer_Dns_Domain` 服务与 {{site.data.keyword.BluSoftlayer_notm}} 权威 DNS 服务器进行交互。 

每个 `SoftLayer_Dns_Domain` 都具有由 `resourceRecords` 关系属性引用的 `SoftLayer_DNS_Domain_ResourceRecords` 集合。可以通过 `SoftLayer_Dns_Domain` 服务与资源记录进行交互；但是，最好在初始区域创建后直接使用 `SoftLayer_Dns_Domain_ResourceRecord` 服务。

## 域
{:#dns-api-domains}
### 列出域
{:#dns-api-listing-domains}
可以使用返回 `SoftLayer_Dns_Domain` 模板对象数组的 `SoftLayer_Account::getDomains` 来检索当前在 {{site.data.keyword.BluSoftlayer_notm}} 名称服务器上托管的所有域的列表。还可以扩展此调用以使用对象掩码来拉取与这些域关联的记录。

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### 创建域
{:#dns-api-creating-domains}
要创建新的区域，必须创建 `SoftLayer_Dns_Domain` 模板对象并将其传递到 `SoftLayer_Dns_Domain::createObject` 中。在创建期间，会自动添加 `ns1.softlayer.com` 和 `ns2.softlayer.com` 的 NS 记录。要成功完成创建操作，该模板对象必须至少包含一个 A 或 AAAA 记录。API 将添加或更新域序列号，因此不需要在模板对象中包含序列号。

创建 `SoftLayer_Dns_Domain` 对象时，以下属性是必需的。
 * name - 域名（包括 TDL“example.com”）
 * resourceRecords - 至少一个 SoftLayer_Dns_Domain_ResourceRecord 的数组
 
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

`SoftLayer_Dns_Domain::createObject` 会返回完全填充的 `SoftLayer_Dns_Domain` 对象。

### 编辑域
{:#dns-api-existing-domains}
无法修改现有的 `SoftLayer_Dns_Domain` 条目。对区域名称的更改应重构为创建新区域。

### 删除域
{:#dns-api-deleting-domains}
使用 `SoftLayer_Dns_Domain::deleteObject` 来除去区域。此方法仅需要提供 init 参数。

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` 会返回布尔值：`true` 表示成功，`false` 表示失败。

## 记录
{:#dns-api-records}
### 列出记录
{:#dns-api-listing-records}
除了上面提到的方法外，还可以使用返回 `SoftLayer_Dns_DomainResourceRecord` 对象数组的 `SoftLayer_Dns_Domain::getResourceRecords` 来检索域资源记录。

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### 创建记录
{:#dns-api-creating-records}
通过 `SoftLayer_Dns_Domain_ResourceRecord` 服务直接创建记录是借助创建 `SoftLayer_Dns_Domain_ResourceRecord` 模板对象并将其传递到 `SoftLayer_Dns_Domain_ResourceRecord::createObject` 中来完成的。主机属性中使用的“@”表示通配符主机名。

{{site.data.keyword.BluSoftlayer_notm}} DNS 系统支持以下记录类型：
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

模板对象必须至少包含：
 * data - 记录的值
 * host - 要在区域下添加的标签
  
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

### 编辑记录
{:#dns-api-editing-records}
通过将模板对象传递到 `SoftLayer_Dns_Domain_ResourceRecord::editObject` 中来编辑资源记录。模板对象必须包含：

 * id - 要编辑的 `SoftLayer_Dns_Domain_ResourceRecord` 的标识。
 * domainId - 此资源记录是其子记录的 `SoftLayer_Dns_Domain` 的标识
 * 要更改的属性。[注：域序列号由 API 自动更新。]
  
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
还必须使用资源记录标识属性来填充 init 参数。`SoftLayer_Dns_Domain_ResourceRecord::editObject` 会返回布尔值

### 删除记录
{:#dns-api-deleting-records}
使用 `SoftLayer_Dns_Domain_ResourceRecord::deleteObject` 来除去记录。此方法仅需要提供 init 参数。

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` 会返回布尔值：`true` 表示成功，`false` 表示失败。
