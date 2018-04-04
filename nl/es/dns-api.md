---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Iniciación a la API de DNS￼

Los usuarios pueden interactuar con los servidores DNS autorizados de {{site.data.keyword.BluSoftlayer_notm}} mediante el servicio `SoftLayer_Dns_Domain`. 

Cada `SoftLayer_Dns_Domain` tiene un grupo de `SoftLayer_DNS_Domain_ResourceRecords` a los que hace referencia la propiedad relacional `resourceRecords`. Se puede interactuar con registros de recursos a través del servicio `SoftLayer_Dns_Domain`; sin embargo, es mejor utilizar el servicio `SoftLayer_Dns_Domain_ResourceRecord` directamente después de la creación de la zona inicial.

## Dominios
### Listado
Se puede recuperar una lista de todos los dominios actualmente alojados en servidores de nombres de {{site.data.keyword.BluSoftlayer_notm}} con `SoftLayer_Account::getDomains`, que devuelve una matriz de objetos de plantilla `SoftLayer_Dns_Domain`. También puede ampliar esta llamada para recuperar los registros asociados con estos dominios utilizando una máscara de objeto.

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### Creación
Para crear una zona nueva, se debe crear un objeto de plantilla `SoftLayer_Dns_Domain` y se
debe pasar a `SoftLayer_Dns_Domain::createObject`. Los registros NS correspondientes a `ns1.softlayer.com` y `ns2.softlayer.com` se añaden automáticamente durante la creación. Incluya al menos un registro A o AAAA con el objeto de plantilla para garantizar una creación correcta. La API añadirá o actualizará los números de serie del dominio, así que no hace falta incluirlos en el objeto de plantilla.

Se necesitan las siguientes propiedades cuando se crea un objeto `SoftLayer_Dns_Domain`.
 * name - Nombre de dominio que incluye el TDL "example.com"
 * resourceRecords - Una matriz de al menos un SoftLayer_Dns_Domain_ResourceRecord
 
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

`SoftLayer_Dns_Domain::createObject` devuelve un objeto `SoftLayer_Dns_Domain` con información.

### Edición
No se pueden modificar las entradas `SoftLayer_Dns_Domain` existentes. Los cambios en nombres de zona se deben realizar mediante la creación de zonas nuevas.

### Supresión
La eliminación de una zona se realiza mediante `SoftLayer_Dns_Domain::deleteObject`. Este método solo requiere que se especifique un parámetro init.

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` devuelve un valor booleano: `true` si la operación se realiza correctamente, `false` en caso contrario.

## Registros
### Listado
Además del método mencionado anteriormente, los registros de recursos de dominio se pueden recuperar con `SoftLayer_Dns_Domain::getResourceRecords`, que devuelve una matriz de `objetos SoftLayer_Dns_DomainResourceRecord`.

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### Creación
Para crear registros directamente mediante el servicio `SoftLayer_Dns_Domain_ResourceRecord`, hay que crear un objeto de plantilla `SoftLayer_Dns_Domain_ResourceRecord` y pasarlo a `SoftLayer_Dns_Domain_ResourceRecord::createObject`. El signo '@' en la propiedad host indica un nombre de host comodín.

El sistema DNS de {{site.data.keyword.BluSoftlayer_notm}} admite estos tipos de registro:
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

Como mínimo, el objeto de plantilla debe contener:
 * data - valor del registro
 * host - etiqueta que se añadirá bajo la zona
  
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

### Edición
Para editar registros de recurso, pase un objeto de plantilla a `SoftLayer_Dns_Domain_ResourceRecord::editObject`. El objeto de plantilla debe contener:

 * id - identificador del `SoftLayer_Dns_Domain_ResourceRecord` que se va a editar.
 * domainId - identificador del `SoftLayer_Dns_Domain` del que este registro de recurso es un registro hijo
 * propiedades que se van a modificar [Nota: la API actualiza automáticamente los números de serie de dominio.]
  
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
También es necesario especificar información en los parámetros init con la propiedad de ID de recurso. `SoftLayer_Dns_Domain_ResourceRecord::editObject` devuelve un valor booleano

### Supresión
La eliminación de un registro se realiza mediante `SoftLayer_Dns_Domain_ResourceRecord::deleteObject`. Este método solo requiere que se especifique un parámetro init.

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject();
print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` devuelve un valor booleano: `true` si la operación se realiza correctamente, `false` en caso contrario.
