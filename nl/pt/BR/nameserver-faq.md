---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: IBM Cloud name server addresses, Authoritative Name Servers, domain names

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# FAQs do servidor de nomes
{:#nameserver-faqs}

## Quais são os endereços do servidor de nomes do IBM Cloud?
{:#what-are-the-ibm-cloud-name-server-addresses}

Temos dois endereços para Servidores de nomes autorizados e dois endereços para Servidores de nomes de resolução.

**Servidores de nomes autorizados**

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

**Resolvendo servidores de nomes**

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12


## Qual é a diferença entre os servidores de nome públicos e privados no SoftLayer?
{:#what-is-the-difference-public-private-nameserver}

Os servidores de nomes atuam como servidores de nomes autorizados para nomes de domínio que residem em nossos servidores DNS e são gerenciados por meio do Portal do cliente. Esses servidores "respondem" e "resolvem" nomes de domínio para o seu endereço IP para a população da Internet geral.

Os servidores de nomes de resolução estão localizados na rede privada e agem como resolvedores de DNS para o seu servidor. Os resolvedores privados consultam os servidores de nomes raiz da Internet para consultas de domínio. Por exemplo, enviar e-mail de seu servidor requer uma NSlookup do nome de domínio de destino. Os servidores DNS privados resolvem essas informações sobre a rede privada para manterem o uso de sua largura da banda baixo, reduzirem a carga nos servidores autorizados e oferecerem resolução rápida. Resolvedores de rede privada são um serviço de conveniência para nossos clientes.

## Quais são as minhas opções do servidor de nomes?
{:#what-are-my-name-server-options}

Com um Bare Metal Server há quatro opções típicas para servidores de nomes:

1. Use os seus servidores de nomes de escrivão de nome de domínio para gerenciar os seus nomes de domínio.
2. Use servidores de nomes do IBM Cloud para gerenciar os seus nomes de domínio.
3. Use um serviço de DNS de terceiro para gerenciar os seus nomes de domínio.
4. Execute os seus próprios servidores de nomes em seu servidor para gerenciar os seus nomes de domínio.

Para as opções 1, 2 e 3 você usará servidores nomes do terceiro (por exemplo, `ns1.softlayer.com` e `ns2.softlayer.com`). Para a opção número 4, você usará o seu domínio como o servidor de nomes (`ns1.yourdomain.com` e `ns2.yourdomain.com`). A opção número 4 requer que você execute serviços de DNS em seu servidor e você também deve registrar o seu domínio como um servidor de nomes com o seu escrivão. Este registro normalmente é livre, mas ele requer uma etapa adicional além do processo de registro de nome de domínio básico.

O IBM Cloud oferece serviços de DNS livres que são totalmente gerenciados por meio do [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). É altamente recomendado permitir que o IBM Cloud gerencie o seu DNS e aja como os seus servidores de nomes, porque temos sistemas redundantes, facilidade de gerenciamento e a capacidade de resolver problemas relacionados a DNS rapidamente.


## Como posso executar meus próprios servidores de nomes?
{:#how-can-i-run-my-own-nameservers}

A maneira mais fácil de executar e gerenciar os seus próprios servidores de nomes é usar uma ferramenta de painel de controle como **Plesk** ou **cPanel**. Ambos esses produtos foram construídos em servidores de nomes de domínio que permitem incluir, modificar ou excluir nomes de domínio.

Para iniciar, registre o seu nome de domínio como um servidor de nomes com seu escrivão de nome de domínio e designe dois endereços IP por meio dos intervalos de IP de seus servidores.
