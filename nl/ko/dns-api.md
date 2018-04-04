---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS API 시작하기

사용자는 `SoftLayer_Dns_Domain` 서비스를 통해 {{site.data.keyword.BluSoftlayer_notm}} 인증 DNS 서버와 상호작용할 수 있습니다.  

각 `SoftLayer_Dns_Domain`은 `resourceRecords` 관계형 특성에 의해 참조되는 `SoftLayer_DNS_Domain_ResourceRecords`의 콜렉션을 갖고 있습니다. `SoftLayer_Dns_Domain` 서비스를 통해 리소스 레코드와 상호작용할 수 있지만, 초기 구역 작성 후에 `SoftLayer_Dns_Domain_ResourceRecord` 서비스를 직접 사용하는 것이 가장 좋습니다. 

## 도메인
### 나열
현재 {{site.data.keyword.BluSoftlayer_notm}} 이름 서버에 호스팅되는 모든 도메인의 목록은 `SoftLayer_Dns_Domain` 템플리트 오브젝트의 배열을 리턴하는 `SoftLayer_Account::getDomains`을 사용하여 검색할 수 있습니다. 또한 이 호출을 확장하여 오브젝트 마스크를 사용하여 이들 도메인과 연관된 레코드를 가져올 수도 있습니다. 

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### 작성
새 구역을 작성하려면 `SoftLayer_Dns_Domain` 템플리트 오브젝트를 작성하여 `SoftLayer_Dns_Domain::createObject`로 전달해야 합니다. `ns1.softlayer.com` 및 `ns2.softlayer.com`에 대한 NS 레코드가 작성 중에 자동으로 추가됩니다. 성공적인 작성을 위해 템플리트 오브젝트에 하나 이상의 A 또는 AAAA 레코드를 포함하십시오. 도메인 일련 번호는 API에 의해 추가 또는 업데이트되므로 템플리트 오브젝트에 해당 번호를 포함할 필요는 없습니다. 

다음 특성이 `SoftLayer_Dns_Domain` 오브젝트를 작성할 때 필요합니다. 
 * name - TDL "example.com"을 포함하는 도메인 이름
 * resourceRecords - 하나 이상의 SoftLayer_Dns_Domain_ResourceRecord의 배열
 
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

`SoftLayer_Dns_Domain::createObject`는 완전히 채워진 `SoftLayer_Dns_Domain` 오브젝트를 리턴합니다. 

### 편집
기존 `SoftLayer_Dns_Domain` 항목 수정은 불가능합니다. 구역 이름 변경은 새 구역의 작성으로 리팩터링되어야 합니다. 

### 삭제
구역 삭제는 `SoftLayer_Dns_Domain::deleteObject`를 사용하여 수행됩니다. 이 메소드는 init 매개변수만 제공하면 됩니다. 

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject`는 성공의 경우 `true`, 실패의 경우 `false`의 부울 값을 리턴합니다. 

## 레코드
### 나열
위에서 언급한 방법 외에, `SoftLayer_Dns_DomainResourceRecord 오브젝트`의 배열을 리턴하는 `SoftLayer_Dns_Domain::getResourceRecords`를 사용하여 도메인 리소스 레코드를 검색할 수 있습니다. 

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### 작성
`SoftLayer_Dns_Domain_ResourceRecord` 서비스를 통한 직접 레코드 작성은 `SoftLayer_Dns_Domain_ResourceRecord` 템플리트 오브젝트를 작성하고 이를 `SoftLayer_Dns_Domain_ResourceRecord::createObject`로 전달하여 수행됩니다. 호스트 특성에 '@'를 사용하면 와일드카드 호스트 이름이 지정됩니다. 

{{site.data.keyword.BluSoftlayer_notm}} DNS 시스템은 다음의 레코드 유형을 지원합니다. 
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

최소한, 템플리트 오브젝트는 다음을 포함해야 합니다. 
 * data - 레코드의 값
 * host - 구역 아래에 추가되는 레이블
  
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

### 편집
템플리트 오브젝트를 `SoftLayer_Dns_Domain_ResourceRecord::editObject`로 전달하여 리소스 레코드를 편집하십시오. 템플리트 오브젝트는 다음을 포함해야 합니다. 

 * id - 편집할 `SoftLayer_Dns_Domain_ResourceRecord`의 ID
 * domainId - 이 리소스 레코드가 하위 레코드인 `SoftLayer_Dns_Domain`의 ID
 * 변경될 특성 [참고: 도메인 일련 번호는 API에 의해 자동으로 업데이트됩니다.]
  
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
또한 init 매개변수를 리소스 레코드 ID 특성으로 채워야 합니다. `SoftLayer_Dns_Domain_ResourceRecord::editObject`에 의해 부울이 리턴됩니다.

### 삭제
레코드의 제거는 `SoftLayer_Dns_Domain_ResourceRecord::deleteObject`를 사용하여 수행됩니다. 이 메소드는 init 매개변수만 제공하면 됩니다. 

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject`는 성공의 경우 `true`, 실패의 경우 `false`의 부울 값을 리턴합니다. 
