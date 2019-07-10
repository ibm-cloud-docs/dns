---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone Record, Update DNS Zone Record, edit dns zone record, add dns zone record, delete dns zone record 

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Gerenciando registros de Zona de DNS
{: #manage-dns-zone-records}
Esta seção detalha como incluir, editar e excluir Registros de Zona de DNS.

## Incluir um registro de Zona de DNS
{: #add-a-dns-zone-record}

Após [incluir uma Zona de DNS](/docs/infrastructure/dns?topic=dns-manage-dns-zones#add-a-dns-zone), os Registros podem ser incluídos nela a qualquer momento. Esses registros incluem:

* Registros de A (Host)
* Registros de AAAA (Host)
* Registros de CNAME (Alias)
* Registros de MX (Troca de e-mail)
* Registros de TXT (Texto)
* Registros de SRV (Serviço)

Siga as etapas abaixo para incluir um Registro de Zona de DNS:

* Navegue para a tela **Zona de DNS**. Consulte [Usando a tela Zonas do DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens).
* Selecione a Zona de DNS para a qual o registro será incluído.
* Selecione o **tipo de recurso** desejado na lista suspensa de **Tipos de recurso**.
* Complete os campos restantes para o novo Registro. Consulte a tabela abaixo para obter mais informações: <br/><br/><table border="1"><tbody><tr><th scope="col">Tipo de registro</th><th scope="col">Campo</th><th scope="col">Entrada</th></tr><tr><td rowspan="3">A (Host), AAAA (Host) ou CNAME (Alias)</td><td>Host</td><td>Insira o <strong>Nome do host</strong>.</td></tr><tr><td>Aponta para</td><td>Insira o <strong>Endereço IP</strong> para o qual o Registro de host aponta.</td></tr><tr><td>TTL</td><td>Selecione o Tempo de vida (TTL) na lista suspensa. O TTL assume o padrão de 15 minutos.</td></tr><tr><td rowspan="4">MX (Troca de e-mail)</td><td>Prioridade</td><td>Insira a <strong>Prioridade</strong> do host de destino. Quanto menor o número, maior a prioridade.</td></tr><tr><td>Host</td><td>Insira o <strong>Nome do host</strong>.</td></tr><tr><td>Vai</td><td>Insira o <strong>CNAME</strong> do servidor de e-mail. Isso geralmente é representado como `mail.example.com`.</td></tr><tr><td>TTL</td><td>Selecione o Tempo de vida (TTL) na lista suspensa. O TTL assume o padrão de 15 minutos.</td></tr><tr><td rowspan="3">TXT (Texto)</td><td>Nome</td><td>Insira o <strong>@</strong> ou o <strong>Nome de domínio</strong>.</td></tr><tr><td>Valor</td><td>Insira o <strong>registro</strong> para verificar os finais corretos de e-mail apropriado para um domínio ou IP.</td></tr><tr><td>TTL</td><td>Selecione o Tempo de vida (TTL) na lista suspensa. O TTL assume o padrão de 15 minutos.</td></tr><tr><td rowspan="8">SRV (Registro de serviço)</td><td>Serviço</td><td>Insira o <strong>Nome simbólico</strong> do serviço desejado.</td></tr><tr><td>Protocolo</td><td>Selecione o <strong>Protocolo</strong> que está sendo usado na lista suspensa.</td></tr><tr><td>Prioridade</td><td>Insira a <strong>Prioridade</strong> do host de destino. Quanto menor o número, maior a prioridade.</td></tr><tr><td>Peso</td><td>Insira o <strong>Peso relativo</strong> para registros com a mesma prioridade.</td></tr><tr><td>Porta</td><td>Insira o <strong>TCP ou porta UPD</strong> no qual o serviço deve ser localizado.</td></tr><tr><td>Host (opcional)</td><td>Insira o <strong>Nome do host</strong> para o serviço.</td></tr><tr><td>Destino</td><td>Insira o <strong>Nome do host canônico</strong> da máquina que está fornecendo o serviço.</td></tr><tr><td>TTL</td><td>Selecione o Tempo de vida (TTL) na lista suspensa. O TTL assume o padrão de 15 minutos.</td></tr></tbody></table><br/>
* Selecione o botão **Incluir registro** para incluir o novo Registro de zona.

### O que acontece em seguida
{:#add-a-dns-zone-record-next}

Após incluir o Registro de Zona, ele aparece na seção **Registros existentes** da tela. É possível [editar](#edit-a-dns-zone-record) ou [excluir](#delete-a-dns-zone-record) o Registro de zona a qualquer momento.

## Edite um registro de Zona de DNS
{: #edit-a-dns-zone-record}

Registros de Zona de DNS existentes podem ser editados por um usuário para atualizar várias áreas, como Tempo de Vida (TTL), registros de Ponteiro (PTR) e Nomes do host. Vários hosts e aliases podem ser
associados a um Registro de Zona de DNS a qualquer momento. Siga as etapas abaixo para editar um registro de Zona de DNS existente.

* Navegue até a tela **Zona do DNS** desejada selecionando **Infraestrutura Clássica** no menu de navegação. 
* Selecione **Rede > DNS > Zonas de Encaminhamento** no menu de navegação da Infraestrutura Clássica.
* Clique na **linha** que contém qualquer registro existente. 

  Os registros que estão em itálico não podem ser editados. Eles geralmente são limitados
aos registros do NS (servidor de nomes).
  {: note}
  
* Atualize os detalhes do registro conforme necessário.
* Selecione o botão **Atualizar** para atualizar o registro ou selecione **Cancelar** para cancelar a ação.

### O que acontece em seguida
{: #edit-a-dns-zone-record-next}

Ao atualizar o registro, seus detalhes exibirão a nova entrada automaticamente. Os registros podem ser atualizados a qualquer momento, registros existentes podem ser excluídos e novos registros podem ser [incluídos](#add-a-dns-zone-record).

## Excluir um Registro de Zona de DNS
{: #delete-a-dns-zone-record}

A exclusão de um Registro de Zona de DNS é feita por meio da tela **Zona de edição de DNS**. A exclusão de um Registro de Zona de DNS não pode ser desfeita.
* Selecione a Zona de DNS que possui o registro que você deseja excluir clicando no nome na
lista de Zonas de DNS.
* Selecione o ícone Excluir no final da linha que contém o registro desejado. Uma caixa de
confirmação pop-up aparecerá.
* Selecione o botão **Sim** para confirmar a exclusão ou selecione o botão **Não** para cancelar a ação.
