---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Select Basic cPanel, Private Nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Crie servidores de nomes privados em cPanel/WHM
{:#create-private-nameservers-in-cpanel-whm}

Usando o produto cPanel/WHM, é possível criar servidores de nomes privados a qualquer momento. Servidores de nomes privados permitem que os servidores de nomes associados com um website (por exemplo, `www.yourdomain.com`) exibam o servidor de nomes do website (por exemplo, `ns1.yourdomain.com`) em vez do servidor de nomes associado ao host da web para o website (por exemplo `ns1.webhostdomain.com`). Incluir um servidor de nomes privado em um domínio também abre opções adicionais para gerenciamento de DNS dentro do cPanel/WHM. Siga as etapas neste artigo para criar um servidor de nomes privado. Se surgirem problemas durante ou após a execução desse procedimento, [abra um chamado](/docs/get-support?topic=get-support-getting-customer-support).

## Nomeie o servidor de nomes
{:#name-the-nameserver}

* Efetue login no WHM em seu servidor na URL a seguir: `http://xx.xx.xx.xx:2086`.
* Selecione **Configuração básica do cPanel/WHM** no menu **Configuração do servidor**.
* Insira os nomes do host do servidor de nomes desejado em um ou mais dos campos a seguir:
  * Servidor de nomes primário
  * Servidor de nomes secundário
  * Servidor de nomes terciário
  * Servidor de nomes quaternário
* Selecione o botão **Salvar**.

## Crie um Arquivo de zona para o domínio
{:#create-a-zone-file-for-the-domain}

* Selecione **Incluir uma Zona de DNS** no menu **Functions de DNS**.
* Insira o **endereço IP** para o domínio no campo **Ip**.
* Insira o **nome de domínio** no campo **Domínio**.

Como alternativa, uma Conta de Domínio pode ser criada com o guia [Criar uma conta](https://docs.cpanel.net/display/70Docs/Create+a+New+Account) na documentação do WHM do cPanel.
{:note}

## Designe um IP para o servidor de nomes
{:#assign-an-ip-to-the-nameserver}

* Selecione **IPs do servidor de nomes** no menu **Configuração de rede**.
* Insira o primeiro **nome do servidor de nomes** no campo **Servidor de nomes**.
* Selecione o botão **Designar**.
* Repita as etapas acima para cada servidor de nomes.

## Configure o servidor de nomes
{:#setup-the-nameserver}

* Selecione **Configuração do servidor de nomes** no menu **Configuração de serviço**.
* Selecione o botão **Continuar** na mensagem pop-up.
