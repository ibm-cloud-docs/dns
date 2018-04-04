---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Crie servidores de nomes privados em cPanel/WHM

Usando o produto cPanel/WHM, é possível criar servidores de nomes privados a qualquer momento. Servidores de nomes privados permitem que os servidores de nomes associados com um website (por exemplo, `www.yourdomain.com`) exibam o servidor de nomes do website (por exemplo, `ns1.yourdomain.com`) em vez do servidor de nomes associado ao host da web para o website (por exemplo `ns1.webhostdomain.com`). Incluir um servidor de nomes privado em um domínio também abre opções adicionais para gerenciamento de DNS dentro do cPanel/WHM. Siga as etapas neste artigo para criar um servidor de nomes privado. Se surgirem problemas durante ou após a execução deste procedimento, [abra um chamado](/general/create-ticket.html).

## Nomeie o servidor de nomes

* Efetue login no WHM em seu servidor na URL a seguir: http://xx.xx.xx.xx:2086.
* Selecione **Configuração básica do cPanel/WHM** no menu **Configuração do servidor**.
* Insira os nomes do host do servidor de nomes desejado em um ou mais dos campos a seguir:
  * Servidor de nomes primário
  * Servidor de nomes secundário
  * Servidor de nomes terciário
  * Servidor de nomes quaternário
* Selecione o botão **Salvar**.

## Crie um Arquivo de zona para o domínio

* Selecione **Incluir uma Zona de DNS** no menu **Funções de DNS**.
* Insira o **endereço IP** para o domínio no campo **Ip**.
* Insira o **nome de domínio** no campo **Domínio**.

**Nota:** como alternativa, uma Conta de domínio pode ser criada com o guia [Criar uma conta](http://docs.cpanel.net/twiki/bin/view/AllDocumentation/WHMDocs/CreateAccount) na documentação do WHM do cPanel.

## Designe um IP para o servidor de nomes

* Selecione **IPs do servidor de nomes** no menu **Configuração de rede**.
* Insira o primeiro **nome do servidor de nomes** no campo **Servidor de nomes**.
* Selecione o botão **Designar**.
* Repita as etapas acima para cada servidor de nomes.

## Configure o servidor de nomes

* Selecione **Configuração do servidor de nomes** no menu **Configuração de serviço**.
* Selecione o botão **Continuar** na mensagem pop-up.
