---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Terminology, Caching, individual DNS servers, DNS resolver

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Terminologia do DNS
{:#dns-terminology}

## Armazenamento em cache e tempo de vida
{:#caching-and-time-to-live}

Devido ao grande volume de solicitações geradas por um sistema como o DNS, os designers forneceram um mecanismo para reduzir a carga em servidores DNS individuais, conforme a seguir:

Quando um resolvedor de DNS (ou seja, um cliente) recebe uma resposta do DNS, ele armazena em cache essa resposta por um determinado período de tempo, chamado de tempo de vida ou TTL. O valor de TTL é configurado pelo administrador do servidor DNS que estiver distribuindo a resposta. Quando uma resposta entrar no cache, o resolvedor consultará a sua resposta em cache (armazenada); somente quando o TTL expirar (ou quando um administrador limpar manualmente a resposta da memória do resolvedor) o resolvedor entrará em contato com o servidor DNS para as mesmas informações.

## Parâmetros do registro do Start of Authority (SOA)
{:#soa-record-parameters}

Geralmente, o tempo de vida é especificado no registro do Start of Authority (SOA). Os parâmetros do SOA são:

### Serial
{:#soa-record-parameters-serial}

O número de revisão deste arquivo de zona. Incremente esse número sempre que o arquivo de zona mudar para que as mudanças sejam distribuídas para quaisquer servidores DNS secundários.

### Atualizar
{:#soa-record-parameters-refresh}

A quantia de tempo em segundos que um servidor de nomes secundário deve esperar para verificar uma nova cópia de uma zona de DNS do servidor de nomes primário do domínio. Se um arquivo de zona mudar, o servidor DNS secundário atualizará a cópia da zona dele para corresponder à do servidor DNS primário.

### Tente novamente
{:#soa-record-parameters-retry}

O tempo em segundos que um servidor (ou servidores) de nomes primário do domínio deverá esperar se uma tentativa para atualizar por um servidor de nomes secundário tiver falhado antes de tentar atualizar uma zona do domínio com esse servidor de nomes secundário novamente.

### Expirar
{:#soa-record-parameters-expire}

A quantia de tempo em segundos que um servidor (ou servidores) de nomes secundário manterá uma zona antes que não for mais considerada autorizada.

### Mínimo
{:#soa-record-parameters-minimum}

A quantia de tempo em segundos que os registros de recurso de um domínio são válidos. Isso também é conhecido como um TTL mínimo e pode ser substituído por um TTL do registro de recurso individual.

### TTL (tempo de vida)
{:#soa-record-parameters-ttl}

O número de segundos que um nome de domínio é armazenado em cache localmente antes da expiração e retorna para servidores de nomes autorizados para obter informações atualizadas.
