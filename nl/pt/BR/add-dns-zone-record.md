---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Incluir um registro de Zona de DNS

Após [incluir uma Zona de DNS](add-dns-zone.html), os Registros podem ser incluídos nela a qualquer momento. Esses registros incluem:

* Registros de A (Host)
* Registros de AAAA (Host)
* Registros de CNAME (Alias)
* Registros de MX (Troca de e-mail)
* Registros de TXT (Texto)
* Registros de SRV (Serviço)

Siga as etapas abaixo para incluir um Registro de Zona de DNS:

* Navegue para a tela **Zona do DNS** desejada. Consulte [Usando a tela Zonas do DNS](use-dns-zones-screen.html).
* Selecione a Zona de DNS para a qual o registro será incluído.
* Selecione o **tipo de recurso** desejado na lista suspensa de **Tipos de recurso**.
* Complete os campos restantes para o novo Registro. Consulte a tabela abaixo para obter mais informações:<br/><br/><table border="1"><tbody><tr><th>Tipo de registro</th><th>Campo</th><th>Entrada</th></tr><tr><td rowspan="3">A (Host), AAAA (Host) ou CNAME (Alias)</td><td>Host</td><td>Insira o <strong>Nome do host</strong>.</td></tr><tr><td>Aponta para</td><td>Insira o <strong>Endereço IP</strong> para o qual o Registro de host aponta.</td></tr><tr><td>TTL</td><td>Selecione o Tempo de vida (TTL) na lista suspensa. O TTL assume o padrão de 15 minutos.</td></tr><tr><td rowspan="4">MX (Troca de e-mail)</td><td>Prioridade</td><td>Insira a <strong>Prioridade</strong> do host de destino. Quanto menor o número, maior a prioridade.</td></tr><tr><td>Host</td><td>Insira o <strong>Nome do host</strong>.</td></tr><tr><td>Vai</td><td>Insira o <strong>CNAME</strong> do servidor de e-mail. Isso geralmente é representado como mail.example.com.</td></tr><tr><td>TTL</td><td>Selecione o Tempo de vida (TTL) na lista suspensa. O TTL assume o padrão de 15 minutos.</td></tr><tr><td rowspan="3">TXT (Texto)</td><td>Nome</td><td>Insira o <strong>@</strong> ou o <strong>Nome de domínio</strong>.</td></tr><tr><td>Valor</td><td>Insira o <strong>registro</strong> para verificar os finais corretos de e-mail apropriado para um domínio ou IP.</td></tr><tr><td>TTL</td><td>Selecione o Tempo de vida (TTL) na lista suspensa. O TTL assume o padrão de 15 minutos.</td></tr><tr><td rowspan="8">SRV (Registro de serviço)</td><td>Serviço</td><td>Insira o <strong>Nome simbólico</strong> do serviço desejado.</td></tr><tr><td>Protocolo</td><td>Selecione o <strong>Protocolo</strong> que está sendo usado na lista suspensa.</td></tr><tr><td>Prioridade</td><td>Insira a <strong>Prioridade</strong> do host de destino. Quanto menor o número, maior a prioridade.</td></tr><tr><td>Peso</td><td>Insira o <strong>Peso relativo</strong> para registros com a mesma prioridade.</td></tr><tr><td>Porta</td><td>Insira o <strong>TCP ou porta UPD</strong> no qual o serviço deve ser localizado.</td></tr><tr><td>Host (opcional)</td><td>Insira o <strong>Nome do host</strong> para o serviço.</td></tr><tr><td>Destino</td><td>Insira o <strong>Nome do host canônico</strong> da máquina que está fornecendo o serviço.</td></tr><tr><td>TTL</td><td>Selecione o Tempo de vida (TTL) na lista suspensa. O TTL assume o padrão de 15 minutos.</td></tr></tbody></table><br/>
* Selecione o botão **Incluir registro** para incluir o novo Registro de zona.

## O que acontece em seguida

Após incluir o Registro de Zona, ele aparece na seção **Registros existentes** da tela. Você pode [editar](edit-dns-zone-record.html) ou excluir o Registro de Zona a qualquer momento.
