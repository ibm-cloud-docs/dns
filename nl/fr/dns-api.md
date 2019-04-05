---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Domain service, DNS API, resource records

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Initiation à l'API DNS￼
{:#getting-started-with-the-dns-api}

Les utilisateurs peuvent interagir avec les serveurs DNS faisant autorité de {{site.data.keyword.BluSoftlayer_notm}} via le service `SoftLayer_Dns_Domain`. 

Chaque domaine `SoftLayer_Dns_Domain` possède une collection d'enregistrements `SoftLayer_DNS_Domain_ResourceRecords` référencée par la propriété relationnelle `resourceRecords`. Il est possible d'interagir avec les enregistrements de ressources via le service `SoftLayer_Dns_Domain` ; cependant, il est préférable d'utiliser le service `SoftLayer_Dns_Domain_ResourceRecord` directement après la création de la zone initiale.

## Domaines
{:#dns-api-domains}
### Liste de domaines
{:#dns-api-listing-domains}
Vous pouvez extraire une liste de tous les domaines actuellement hébergés sur les serveurs de nom {{site.data.keyword.BluSoftlayer_notm}} à l'aide du service `SoftLayer_Account::getDomains` qui renvoie un tableau d'objets de modèle `SoftLayer_Dns_Domain`. Vous pouvez également étendre cet appel pour extraire les enregistrements associés à ces domaines à l'aide d'un masque d'objet.

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### Création de domaines
{:#dns-api-creating-domains}
Pour créer une nouvelle zone, vous devez créer un objet de modèle `SoftLayer_Dns_Domain` et le transmettre au service `SoftLayer_Dns_Domain::createObject`. Les enregistrements DNS pour `ns1.softlayer.com` et `ns2.softlayer.com` sont automatiquement ajoutés lors de la création. Incluez au moins un enregistrement A ou AAAA avec l'objet de modèle pour une création aboutie. Les numéros de série du domaine sont ajoutés ou mis à jour par l'API, il n'est donc pas nécessaire de les inclure dans l'objet de modèle.

Les propriétés suivantes sont nécessaires lors de la création d'un objet `SoftLayer_Dns_Domain`.
 * name - Nom de domaine incluant le TDL "example.com"
 * resourceRecords - Tableau contenant au moins un enregistrement SoftLayer_Dns_Domain_ResourceRecord
 
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

`SoftLayer_Dns_Domain::createObject` renvoie un objet `SoftLayer_Dns_Domain` rempli.

### Edition de domaines
{:#dns-api-existing-domains}
La modification des entrées `SoftLayer_Dns_Domain` existantes n'est pas possible. Les modifications apportées aux noms de zones doivent être refactorisées pour la création de nouvelles zones.

### Suppression de domaines
{:#dns-api-deleting-domains}
Vous pouvez supprimer une zone à l'aide de `SoftLayer_Dns_Domain::deleteObject`. Cette méthode nécessite uniquement un paramètre init.

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` renvoie une valeur booléenne : `true` pour réussi, `false` pour échoué.

## Enregistrements
{:#dns-api-records}
### Liste d'enregistrements
{:#dns-api-listing-records}
En plus de la méthode mentionnée ci-dessus, vous pouvez extraire les enregistrements de ressources de domaine à l'aide de `SoftLayer_Dns_Domain::getResourceRecords` qui renvoie un tableau d'objets `SoftLayer_Dns_DomainResourceRecord`.

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### Création d'enregistrements
{:#dns-api-creating-records}
La création d'enregistrements directement via le service `SoftLayer_Dns_Domain_ResourceRecord` s'effectue en créant un objet de modèle `SoftLayer_Dns_Domain_ResourceRecord` et en le transmettant à `SoftLayer_Dns_Domain_ResourceRecord::createObject`. L'utilisation de '@' dans la propriété hôte indique un nom d'hôte générique.

Le système DNS {{site.data.keyword.BluSoftlayer_notm}} prend en charge les types d'enregistrement suivants :
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

Au minimum, l'objet de modèle doit contenir :
 * data - valeur de l'enregistrement
 * host - libellé à ajouter sous la zone
  
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

### Edition d'enregistrements
{:#dns-api-editing-records}
Editez les enregistrements de ressources en transmettant un objet de modèle à `SoftLayer_Dns_Domain_ResourceRecord::editObject`. Cet objet modèle doit contenir :

 * id - identifiant de l'enregistrement `SoftLayer_Dns_Domain_ResourceRecord` à éditer.
 * domainId - identifiant du domaine `SoftLayer_Dns_Domain` pour lequel cet enregistrement de ressource est un enregistrement enfant
 * propriétés à modifier [Remarque : les numéros de série des domaines sont automatiquement mis à jour par l'API.]
  
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
Il est également nécessaire de remplir les paramètres init avec la propriété ID d'enregistrement de ressource. Un booléen est renvoyé par `SoftLayer_Dns_Domain_ResourceRecord::editObject`

### Suppression d'enregistrements
{:#dns-api-deleting-records}
Vous pouvez supprimer un enregistrement à l'aide de `SoftLayer_Dns_Domain_ResourceRecord::deleteObject`. Cette méthode nécessite uniquement un paramètre init.

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` renvoie une valeur booléenne : `true` pour réussi, `false` pour échoué.
