---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-13"

keywords: DNS servers, fast domain name resolution, DNS FAQ

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}


# FAQ de DNS
{:#dns-faq}

## Quais são os servidores DNS?
{:#what-are-dns-servers}
{: faq}

161.26.0.10 e 161.26.0.11

## Quais são os resolvedores de DNS locais?
{:#what-are-local-dns-resolvers}
{: faq}

Os servidores de nomes de resolução local em nossa rede privada são:

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Esses servidores de nomes fornecem resolução de nome de domínio rápida que não usa a sua dotação de largura da banda pública. Para usá-los, siga o procedimento correto para incluir servidores de nomes de resolução em seu sistema operacional.

## Quais são os endereços do servidor de nomes do {{site.data.keyword.BluSoftlayer_notm}}?
{:#what-are-name-server-addresses}
{: faq}

Temos dois endereços para Servidores de nomes autorizados e dois endereços para Servidores de nomes de resolução.

### Servidores de nomes autorizados
{:#authoratative-name-servers}

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### Resolvendo servidores de nomes
{:#resolving-name-servers}

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Esses servidores de nomes de resolução locais estão em nossa rede privada; portanto, eles não usam a sua dotação de largura da banda pública. 

## O que os servidores DNS do IBM Cloud responderão para os meus domínios secundários?
{:#what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}

O Anycast do {{site.data.keyword.BluSoftlayer_notm}}, Servidores DNS autorizados ativados por Protocolo da Internet responderão para os seus domínios secundários. Esses servidores são localizados nos endereços a seguir:

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## Quais endereços IP serão usados para as minhas transferências de zona de domínio secundária.
{:#which-ipaddresses-secondary-domain-zone-transfers}
{: faq}

Transferências para os seus domínios secundários virão de um dos quatro endereços IP a seguir:

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## Qual é a diferença entre os servidores de nomes públicos e privados?
{:#public-v-private-nameservers}
{: faq}

Os nossos servidores de nomes públicos agem como servidores de nomes autorizados para nomes de domínio que residem em nossos servidores DNS e são gerenciados por meio do [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). Esses servidores "respondem" e "resolvem" nomes de domínio para o seu endereço IP para a população da Internet geral.

Os nossos servidores de nomes de resolução estão localizados na rede privada e agem como resolvedores de DNS para o seu servidor. Os resolvedores privados consultam os servidores de nomes raiz da Internet para consultas de domínio. Por exemplo, enviar e-mail de seu servidor requer uma NSlookup do nome de domínio de destino. Os servidores DNS privados resolvem essas informações sobre a rede privada para manterem o uso de sua largura da banda baixo, reduzirem a carga nos servidores autorizados e oferecerem resolução rápida. Resolvedores de rede privada são um serviço de conveniência para nossos clientes.

## Quais são as minhas opções do servidor de nomes?
{:#what-are-my-name-server-options-faq}
{: faq}

Com um Bare Metal Server há quatro opções típicas para servidores de nomes:

* Use os seus servidores de nomes do escrivão de nome de domínio para gerenciar os seus nomes de domínio.
* Use os servidores de nomes do {{site.data.keyword.BluSoftlayer_notm}} para gerenciar os seus nomes de domínio.
* Use um serviço de DNS de terceiro para gerenciar os seus nomes de domínio.
* Execute os seus próprios servidores de nomes em seu servidor para gerenciar os seus nomes de domínio.

Para as primeiras três opções, você usará servidores de nomes do terceiro (por exemplo, `ns1.softlayer.com` e `ns2.softlayer.com`). A última opção usa o seu domínio como o servidor de nome (por exemplo, `ns1.yourdomain.com` e `ns2.yourdomain.com`) e ela requer que você execute serviços de DNS em seu servidor. Também deve-se registrar o seu domínio como um servidor de nomes com o seu escrivão. O registro do servidor de nomes geralmente é livre, mas requer uma etapa adicional além do processo de registro de domínio básico.

Nossos clientes têm livres serviços de DNS que são completamente gerenciados por meio do [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). É altamente recomendado permitir que o {{site.data.keyword.BluSoftlayer_notm}} gerencie o seu DNS e os seus servidores de nomes, devido aos nossos sistemas redundantes, à facilidade de gerenciamento e à capacidade de solucionar problemas relacionados a DNS rapidamente.

## Como eu configuro o meu DNS reverso?
{:#how-do-i-setup-reverse-dns}
{: faq}

A configuração do DNS reverso ocorre usando o nosso [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). Para obter instruções sobre como configurar o seu DNS reverso, consulte [Atualizar um registro de DNS reverso](/docs/infrastructure/dns?topic=dns-update-a-reverse-dns-record).


## Quanto tempo leva para as mudanças de DNS se propagarem?
{:#how-long-for-dns-changes-propagate}
{: faq}

Os tempos de propagação de mudança de DNS dependem da configuração de tempo de vida (TTL) para o registro de DNS.

O TTL padrão é um dia, o que significa que qualquer modificação de um nome de domínio leva um dia para se propagar ao longo da Internet inteira. O TTL poderá ser reduzido se você planejar fazer mudanças frequentemente; no entanto, quanto menor for o TTL, maior a carga se tornará no servidor de nomes. Cargas mais altas têm um potencial de aumentar o tempo de resposta para usuários finais, o que pode impactar a sua satisfação geral.

Quanto maior a configuração de TTL, maior será o desempenho de DNS devido ao armazenamento em cache do ISP local. Quanto menor a configuração de TTL, o desempenho de DNS será menor devido à resolução de nome aumentada.

Para verificar o TTL, verifique o registro do Start of Authority (SOA) para o domínio. Uma ótima ferramenta para revisar informações de domínio é oferecida pelo [CentralOps.net ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://centralops.net/co/)

O TTL é listado em segundos. Divida por 60 para converter o TTL em minutos ou por 3600 para converter em horas.


## Após transferir um domínio, quanto tempo leva para o domínio e as mudanças feitas se tornarem visíveis?
{:#how-long-transfer-change-visiblity}
{: faq}

O seu domínio e/ou as mudanças nele serão visíveis em servidores DNS do IBM Cloud imediatamente após a conclusão da transferência. Devido à natureza da propagação de DNS, haverá um atraso antes que as mudanças fiquem visíveis em outros servidores DNS.

## Posso concluir as solicitações do AXFR na rede privada?
{:#axfr-request-private-network}
{: faq}

Atualmente, o {{site.data.keyword.BluSoftlayer_notm}} não suporta a solicitação do AXFR na rede privada. Todas as solicitações do AXFR devem ser concluídas na rede pública.
