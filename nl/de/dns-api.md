---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Domain service, DNS API, resource records

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Einführung in die DNS-API
{:#getting-started-with-the-dns-api}

Benutzer können über den Service `SoftLayer_Dns_Domain` mit den maßgeblichen {{site.data.keyword.BluSoftlayer_notm}}-DNS-Servern interagieren. 

Jede `SoftLayer_Dns_Domain` verfügt über eine Sammlung von Datensätzen des Typs `SoftLayer_DNS_Domain_ResourceRecords`, die von der relationalen Eigenschaft `resourceRecords` referenziert werden. Obwohl der Service `SoftLayer_Dns_Domain` die Interaktion mit Ressourcendatensätzen ermöglicht, sollte stattdessen der Service `SoftLayer_Dns_Domain_ResourceRecord` unmittelbar nach der ursprünglichen Zonenerstellung verwendet werden.

## Domänen
{:#dns-api-domains}
### Domänen auflisten
{:#dns-api-listing-domains}
Eine Liste aller Domänen, die gegenwärtig auf den {{site.data.keyword.BluSoftlayer_notm}}-Namensservern gehostet werden,
kann mit `SoftLayer_Account::getDomains` abgerufen werden. Dieser Aufruf liefert ein Array mit den
`SoftLayer_Dns_Domain`-Vorlagenobjekten. Sie können diesen Aufruf erweitern, um mithilfe einer Objektmaske
auch die Datensätze zu extrahieren, die diesen Domänen zugeordnet sind.

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### Domänen erstellen
{:#dns-api-creating-domains}
Um eine  neue Zone zu erstellen, muss ein Vorlagenobjekt `SoftLayer_Dns_Domain` erstellt und an `SoftLayer_Dns_Domain::createObject` übergeben werden. Namensserverdatensätze für `ns1.softlayer.com` und `ns2.softlayer.com` werden bei der Erstellung automatisch hinzugefügt. Schließen Sie in das Vorlagenobjekt mindestens einen Datensatz A oder AAAA ein, damit die Erstellung erfolgreich ausgeführt werden kann. Die Domänenseriennummern werden von der API hinzugefügt bzw. aktualisiert, h. h. sie müssen nicht im Vorlagenobjekt angegeben werden.

Beim Erstellen eines Objekts `SoftLayer_Dns_Domain` sind die folgenden Eigenschaften erforderlich.
 * name - Domänenname einschließlich der TDL "example.com"
 * resourceRecords - Ein Array mit mindestens einem Objekt 'SoftLayer_Dns_Domain_ResourceRecord'
 
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

`SoftLayer_Dns_Domain::createObject` gibt ein vollständig bestücktes Objekt `SoftLayer_Dns_Domain` zurück.

### Domänen bearbeiten
{:#dns-api-existing-domains}
Vorhandene Einträge `SoftLayer_Dns_Domain` können nicht geändert werden. Um Zonennamen zu ändern, müssen neue Zonen erstellt werden.

### Domänen löschen
{:#dns-api-deleting-domains}
Das Entfernen einer Zone kann mit dem Aufruf `SoftLayer_Dns_Domain::deleteObject` durchgeführt werden. Bei dieser Methode muss nur ein Initialisierungsparameter angegeben werden.

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` gibt einen booleschen Wert zurück: `true` für Erfolg und `false` für Fehlschlag.

## Datensätze
{:#dns-api-records}
### Datensätze auflisten
{:#dns-api-listing-records}
Neben der oben genannten Methode können Domänenressourcendatensätze auch mit dem Aufruf `SoftLayer_Dns_Domain::getResourceRecords` abgerufen werden, der ein Array mit Objekten des Typs `SoftLayer_Dns_DomainResourceRecord` zurückgibt.

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### Datensätze erstellen
{:#dns-api-creating-records}
Die direkte Erstellung von Datensätzen durch den Service `SoftLayer_Dns_Domain_ResourceRecord` kann durch das Erstellen eines Vorlagenobjekts `SoftLayer_Dns_Domain_ResourceRecord` und das Weitergeben dieses Objekts an `SoftLayer_Dns_Domain_ResourceRecord::createObject` ausgeführt werden. Die Angabe '@' in der Hosteigenschaft bezeichnet einen Platzhalter für den Hostnamen.

Das {{site.data.keyword.BluSoftlayer_notm}}-DNS-System unterstützt die folgenden Datensatztypen:
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

Das Vorlagenobjekt muss mindestens Folgendes enthalten:
 * data: der Wert des Datensatzes
 * host: die Bezeichnung, die in der Zone hinzugefügt werden soll
  
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

### Datensätze bearbeiten
{:#dns-api-editing-records}
Bearbeiten Sie Ressourcendatensätze, indem Sie ein Vorlagenobjekt an `SoftLayer_Dns_Domain_ResourceRecord::editObject` übergeben. Das Vorlagenobjekt muss Folgendes enthalten:

 * id: Die ID des zu bearbeitenden Objekts `SoftLayer_Dns_Domain_ResourceRecord`
 * domainId: Die ID des Objekts `SoftLayer_Dns_Domain`, dem diese Ressource als untergeordneter Datensatz zugeordnet ist
 * Die Eigenschaften, die geändert werden sollen [Hinweis: Domänenseriennummern werden von der API automatisch aktualisiert.]
  
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
Außerdem müssen die Initialisierungsparameter mit der ID-Eigenschaft des Ressourcendatensatzes bestückt werden. Von `SoftLayer_Dns_Domain_ResourceRecord::editObject` wird ein boolescher Wert zurückgegeben.

### Datensätze löschen
{:#dns-api-deleting-records}
Das Entfernen eines Datensatzes kann mit dem Aufruf `SoftLayer_Dns_Domain_ResourceRecord::deleteObject` ausgeführt werden. Bei dieser Methode muss nur ein Initialisierungsparameter angegeben werden.

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` gibt einen booleschen Wert zurück: `true` bei Erfolg und `false` bei Fehlschlag.
