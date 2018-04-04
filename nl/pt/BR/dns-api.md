---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Introdução à API de DNS￼

Os usuários podem interagir com os servidores DNS autorizados {{site.data.keyword.BluSoftlayer_notm}} por meio do serviço `SoftLayer_Dns_Domain`. 

Cada `SoftLayer_Dns_Domain` tem uma coleção de `SoftLayer_DNS_Domain_ResourceRecords` referenciada pela propriedade relacional `resourceRecords`. É possível interagir com os registros de recurso por meio do serviço `SoftLayer_Dns_Domain`; no entanto, é melhor usar o serviço `SoftLayer_Dns_Domain_ResourceRecord` diretamente após a criação de zona inicial.

## Domínios
### Listando
Uma lista de todos os domínios atualmente hospedados nos servidores de nomes do {{site.data.keyword.BluSoftlayer_notm}} pode ser recuperada com o `SoftLayer_Account::getDomains` que retorna uma matriz de objetos de modelo `SoftLayer_Dns_Domain`. É possível estender essa chamada também para puxar os registros associados a esses domínios usando uma máscara de objeto.

```
$client = SoftLayer_SoapClient::getClient('SoftLayer_Account', null, $apiUser, $apiKey);
$objectMask = "mask.resourceRecords";
$client->setObjectMask($objectMask);
$domains = $client->getDomains();
print_r($domains);
```

### criando
Para criar uma nova zona, um objeto de modelo `SoftLayer_Dns_Domain` deve ser criado e passado no `SoftLayer_Dns_Domain::createObject`. Registros do NS para `ns1.softlayer.com` e `ns2.softlayer.com` são incluídos automaticamente durante a criação. Inclua pelo menos um registro A ou AAAA com o objeto de modelo para criação bem-sucedida. Os números de série do domínio serão incluídos ou atualizados pela API; portanto, não há necessidade de incluí-los no objeto de modelo.

As propriedades a seguir são necessárias ao criar um objeto `SoftLayer_Dns_Domain`.
 * nome - nome de domínio, incluindo o TDL "exemplo.com"
 * resourceRecords - uma matriz de pelo menos um SoftLayer_Dns_Domain_ResourceRecord
 
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

`SoftLayer_Dns_Domain::createObject` retorna um objeto `SoftLayer_Dns_Domain` completamente preenchido.

### Editando
Modificar entradas `SoftLayer_Dns_Domain` existentes não é possível. As mudanças em nomes de zona devem ser refatoradas para criação de novas zonas.

### Excluindo
A remoção de uma zona é realizada com `SoftLayer_Dns_Domain::deleteObject`. Esse método requer que apenas um parâmetro init seja fornecido.

```
$domainId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->deleteObject(); print_r($result);

```

`SoftLayer_Dns_Domain::deleteObject` retorna um valor Booleano: `true` para bem-sucedido, `false` para com falha.

## Registros
### Listando
Além do método mencionado acima, os registros de recurso de domínio podem ser recuperados com `SoftLayer_Dns_Domain::getResourceRecords` que retorna uma matriz de `SoftLayer_Dns_DomainResourceRecord objects`.

```
$domainId = 12345;
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain', $domainId, $apiUser, $apiKey);
 
$result = $client->getResourceRecords();
print_r($result);
```

### criando
A criação de registros diretamente por meio do serviço `SoftLayer_Dns_Domain_ResourceRecord` é realizada criando um objeto de modelo `SoftLayer_Dns_Domain_ResourceRecord` e passando-o no `SoftLayer_Dns_Domain_ResourceRecord::createObject`. O uso de '@' na propriedade do host denota um nome do host curinga.

O sistema DNS do {{site.data.keyword.BluSoftlayer_notm}} suporta estes tipos de registro:
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

No mínimo, o objeto de modelo deve conter:
 * dados - valor do registro
 * host - rótulo a ser incluído sob a zona
  
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

### Editando
Edite registros de recurso passando um objeto de modelo em `SoftLayer_Dns_Domain_ResourceRecord::editObject`. O objeto de modelo deve conter:

 * id - identificador para o `SoftLayer_Dns_Domain_ResourceRecord` a ser editado.
 * domainId - identificador do `SoftLayer_Dns_Domain` para o qual esse registro de recurso é um registro de filho
 * propriedades a serem mudadas [Nota: números de série de domínio são atualizados pela API automaticamente.]
  
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
Também é necessário preencher os parâmetros init com a propriedade de ID do registro de recurso. Um booleano é retornado por `SoftLayer_Dns_Domain_ResourceRecord::editObject`

### Excluindo
A remoção de um registro é realizada com `SoftLayer_Dns_Domain_ResourceRecord::deleteObject`. Esse método requer que apenas um parâmetro init seja fornecido.

```
$recordId = 1545925;
 
$client = SoftLayer_SoapClient::getClient('SoftLayer_Dns_Domain_ResourceRecord', $recordId, $apiUser, $apiKey);
 
$result = $client->deleteObject(); print_r($result);
```

`SoftLayer_Dns_Domain_ResourceRecord::deleteObject` retorna um valor Booleano: `true` para bem-sucedido, `false` para com falha.
