---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Getting started with the DNS API￼

Users can interact with the {{site.data.keyword.BluSoftlayer_notm}} authoritative DNS servers through the `SoftLayer_Dns_Domain` service. 

Each `SoftLayer_Dns_Domain` has a collection of `SoftLayer_DNS_Domain_ResourceRecords` referenced by the `resourceRecords` relational property. It is possible to interact with resource records through the `SoftLayer_Dns_Domain` service; however, it is best to use the `SoftLayer_Dns_Domain_ResourceRecord` service directly after initial zone creation.

## Domains
### Listing domains
A list of all domains currently hosted on the {{site.data.keyword.BluSoftlayer_notm}} nameservers can be retrieved with `SoftLayer_Account::getDomains` which returns an array of `SoftLayer_Dns_Domain` template objects. You can extend this call also to pull the records associated with these domains using an object mask.

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### Creating domains
To create a new zone, a `SoftLayer_Dns_Domain` template object must be created and passed into `SoftLayer_Dns_Domain::createObject`. NS records for `ns1.softlayer.com` and `ns2.softlayer.com` are automatically added during creation. Include at least one A or AAAA record with the template object for successful creation. Domain serial numbers will be added or updated by the API so there is no need to include them in the template object.

The following properties are necessary when creating a `SoftLayer_Dns_Domain` object.
 * name - Domain name including the TDL "example.com"
 * resourceRecords - An array of at least one SoftLayer_Dns_Domain_ResourceRecord
 
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

`SoftLayer_Dns_Domain::createObject` returns a fully populated `SoftLayer_Dns_Domain` object.

### Editing domains
Modifying existing `SoftLayer_Dns_Domain` entries is not possible. Changes to zone names should be refactored to creation of new zones.

### Deleting domains
Removal of a zone is accomplished with `SoftLayer_Dns_Domain::deleteObject`. This method requires only an init parameter to be provided.

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` returns a Boolean value: `true` for successful, `false` for failed.

## Records
### Listing records
In addition to the method mentioned above, domain resource records can be retrieved with `SoftLayer_Dns_Domain::getResourceRecords` which returns an array of `SoftLayer_Dns_DomainResourceRecord objects`.

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### Creating records
Creating records directly through the `SoftLayer_Dns_Domain_ResourceRecord` service is accomplished by creating a `SoftLayer_Dns_Domain_ResourceRecord` template object and passing it into `SoftLayer_Dns_Domain_ResourceRecord::createObject`. The use of '@' in the host property denotes a wildcard hostname.

The {{site.data.keyword.BluSoftlayer_notm}} DNS system supports these record types:
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

At minimum, the template object must contain:
 * data - value of the record
 * host - label to be added under the zone
  
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

### Editing records
Edit resource records by passing a template object into `SoftLayer_Dns_Domain_ResourceRecord::editObject`. The template object must contain:

 * id - identifier for the `SoftLayer_Dns_Domain_ResourceRecord` to be edited.
 * domainId - identifier of the `SoftLayer_Dns_Domain` to which this resource record is a child record
 * properties to be changed [Note: Domain serial numbers are updated by the API automatically.]
  
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
It is also necessary to populate the init params with the resource record ID property. A Boolean is returned by `SoftLayer_Dns_Domain_ResourceRecord::editObject`

### Deleting records
Removal of a record is accomplished with `SoftLayer_Dns_Domain_ResourceRecord::deleteObject`. This method requires only an init parameter to be provided.

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` returns a Boolean value: `true` for successful, `false` for failed.
