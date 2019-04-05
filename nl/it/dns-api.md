---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Domain service, DNS API, resource records

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introduzione al'API DNS
{:#getting-started-with-the-dns-api}

Gli utenti possono interagire con i server DNS autorevoli di {{site.data.keyword.BluSoftlayer_notm}} tramite il servizio `SoftLayer_Dns_Domain`. 

Ogni `SoftLayer_Dns_Domain` ha una raccolta di `SoftLayer_DNS_Domain_ResourceRecords` a cui fa riferimento la proprietà relazionale `resourceRecords`. È possibile interagire con i record di risorsa tramite il servizio `SoftLayer_Dns_Domain`; tuttavia, è meglio utilizzare il servizio `SoftLayer_Dns_Domain_ResourceRecord` direttamente dopo la creazione della zona iniziale.

## Domini
{:#dns-api-domains}
### Elenco dei domini
{:#dns-api-listing-domains}
Un elenco di tutti i domini attualmente ospitati sui server dei nomi {{site.data.keyword.BluSoftlayer_notm}} può essere richiamato con `SoftLayer_Account::getDomains`, che restituisce un array di oggetti modello `SoftLayer_Dns_Domain`. Puoi estendere questa chiamata in modo da estrarre i record associati a questi domini utilizzando una maschera oggetto.

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### Creazione dei domini
{:#dns-api-creating-domains}
Per creare una nuova zona, è necessario creare un oggetto modello `SoftLayer_Dns_Domain` template e passarlo in `SoftLayer_Dns_Domain::createObject`. I record di server dei nomi (NS, name server) per `ns1.softlayer.com` e `ns2.softlayer.com` vengono aggiunti automaticamente durante la creazione. Perché l'operazione di creazione venga eseguita correttamente, includi almeno un record A o AAAA con l'oggetto modello. I numeri di serie dominio saranno aggiunti o aggiornati dall'API e, pertanto, non è necessario includerli nell'oggetto modello.

Le seguenti proprietà sono necessarie quando si crea un oggetto `SoftLayer_Dns_Domain`.
 * name - il nome dominio compreso il TDL "example.com"
 * resourceRecords - un array di almeno un SoftLayer_Dns_Domain_ResourceRecord
 
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

`SoftLayer_Dns_Domain::createObject` restituisce un oggetto `SoftLayer_Dns_Domain` completamente compilato.

### Modifica dei domini
{:#dns-api-existing-domains}
La modifica di voci `SoftLayer_Dns_Domain` esistenti non è possibile. Le modifiche ai nomi di zona devono essere riorganizzate in una creazione di nuove zone.

### Eliminazione dei domini
{:#dns-api-deleting-domains}
La rimozione di una zona viene eseguita con `SoftLayer_Dns_Domain::deleteObject`. Questo metodo richiede che venga fornito solo un parametro init.

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` restituisce un valore booleano: `true` per operazione riuscita, `false` per operazione non riuscita.

## Record
{:#dns-api-records}
### Elenco dei record
{:#dns-api-listing-records}
Oltre al metodo summenzionato, i record risorsa di dominio possono essere richiamati con `SoftLayer_Dns_Domain::getResourceRecords` che restituisce un array di `SoftLayer_Dns_DomainResourceRecord objects`.

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### Creazione dei record
{:#dns-api-creating-records}
La creazione di record direttamente tramite il servizio `SoftLayer_Dns_Domain_ResourceRecord` viene eseguita creando un oggetto modello `SoftLayer_Dns_Domain_ResourceRecord` e passandolo in `SoftLayer_Dns_Domain_ResourceRecord::createObject`. L'uso di '@' nella proprietà host denota un nome host jolly.

Il sistema DNS di {{site.data.keyword.BluSoftlayer_notm}} supporta questi tipi di record:
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

Come minimo, l'oggetto modello deve contenere:
 * data - il valore del record
 * host - l'etichetta da aggiungere sotto la zona
  
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

### Modifica dei record
{:#dns-api-editing-records}
Modifica i record risorsa passando un oggetto modello in `SoftLayer_Dns_Domain_ResourceRecord::editObject`. L'oggetto modello deve contenere:

 * id - l'identificativo per il `SoftLayer_Dns_Domain_ResourceRecord` da modificare.
 * domainId - l'identificativo del `SoftLayer_Dns_Domain` di cui questo record risorsa è un record secondario
 * proprietà da modificare [nota: i numeri di serie dominio vengono aggiornati dall'API automaticamente].
  
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
È anche necessario compilare i parametri init con la proprietà di ID record risorsa. Un booleano viene restituito da `SoftLayer_Dns_Domain_ResourceRecord::editObject`

### Eliminazione dei record
{:#dns-api-deleting-records}
La rimozione di un record viene eseguita con `SoftLayer_Dns_Domain_ResourceRecord::deleteObject`. Questo metodo richiede che venga fornito solo un parametro init.

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` restituisce un valore booleano: `true` per operazione riuscita, `false` per operazione non riuscita.
