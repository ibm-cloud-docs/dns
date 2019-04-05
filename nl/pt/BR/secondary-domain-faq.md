---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-07"

keywords: Secondary Domain FAQ, zone transfers, IBM Cloud DNS servers

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQ de domínio secundário
{:#secondary-domain-faq}

## O que os servidores DNS do IBM Cloud responderão para os meus domínios secundários?
{:#what-ibm-cloud-dns-servers-will-answer-for-my-secondary-domains}

Anycast do IBM Cloud, ativado pelo Protocolo da Internet versão 6, Servidores DNS autorizados:

 * ns1.softlayer.com
 * ns2.softlayer.com

## De onde vêm as transferências de zona?
{:#where-will-the-zone-transfers-come-from}

As transferências de seu domínio secundário virão de um dos quatro endereços IP:

  * 66.228.118.67
  * 67.228.119.235
  * 208.43.119.235
  * 12.96.161.249

## Quanto tempo, depois de transferir um domínio, leva para esse domínio ou as mudanças nele ficarem visíveis?
{:#how-long-does-it-take-for-changes-to-become-visible}

O domínio e quaisquer mudanças nele ficarão visíveis em servidores DNS do IBM Cloud imediatamente após a conclusão da transferência. Devido à natureza em cache e propagação de DNS, pode demorar um tempo para que essas mudanças fiquem visíveis em outros servidores DNS.  

## As notificações de atualização de zona são suportadas?
{:#are-zone-update-notifies-supported}

Notificações não são suportadas neste momento.

## Quão imediato é o botão Transferir agora?
{:#how-immediate-is-the-transfer-now-button}

Depois que o botão Transferir agora for clicado, o domínio será transferido no início do próximo minuto.

## Pode um mestre ser configurado na rede privada ou ele terá que passar pela pública?
{:#can-a-master-be-configured-on-private-network}

Não no momento. Todas as solicitações do AXFR são feitas sobre a rede pública.

## Os escravos são removidos após uma série de dias em que o mestre está indisponível?
{:#are-slaves-removed-after-days-master-is-unavailable}

Nós pararemos de tentar transferir um domínio se o seu mestre estiver inativo ou mal configurado por um período prolongado.  O portal fornecerá feedback do cliente (a guia Mensagens de erro) e um método de reativar um domínio (a guia Transferência de zona manual) no evento de haver problemas ao transferir a zona e ele será desativado como uma consequência.

## É 1 minuto a frequência mínima de transferência?
{:#is-1minute-lowest-transfer-frequency}

Sim.

## Se a frequência for configurada como 1920 minutos, então, de volta para 10, os 1920 minutos precisarão expirar antes de a nova frequência entrar em vigor?
{:#frequency-change-expiration-effects}

Não. O sistema calculará a fila de retransferência tomando o tempo da nossa última tentativa de transferência e incluindo a frequência nele.  Então, se você tiver a frequência configurada para 1920 e, então, mudá-la para 10 minutos, contanto que tenha pelo menos 10 minutos desde a última vez que tentou transferir, nós tentaremos de novo imediatamente e, então, a cada 10 minutos daí em diante.
