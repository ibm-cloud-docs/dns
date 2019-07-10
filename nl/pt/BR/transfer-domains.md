---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-15"

keywords: Transfer Existing Domain, Transfer multiple domains 

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Transferir domínios
{: #transfer-domains}

## Transferir domínios existentes para o IBM Cloud
{:#transfer-an-existing-domain-to-ibm-cloud}

Após um domínio ter sido registrado, ele poderá ser transferido a qualquer momento. Transferir um domínio de um escrivão de terceiro para o {{site.data.keyword.cloud}} pode simplificar o processo de gerenciamento de domínio. Transferir um domínio não afeta o website, o e-mail ou o DNS. Só muda o escrivão que gerencia os registros de domínio. Siga as etapas neste artigo para transferir um domínio existente para o {{site.data.keyword.cloud_notm}}.

## Transferir um único domínio
{: #transfer-single-domain}

* Navegue para a tela **Registro de domínio** no [{{site.data.keyword.cloud_notm}} Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). Consulte [Acessar a tela Registro de domínio](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen).
* Escolha a guia **Transferir**.
* Insira o nome de domínio existente no campo **Nome de domínio**.
* Selecione o tipo de domínio na lista suspensa de **Tipos de domínio**.
* Selecione a quantia de tempo pela qual o domínio permanecerá ativo na lista suspensa de **Tempo de registro**.

  O preço para cada período de tempo é exibido ao lado do tempo e será cobrado no cartão de crédito ou deduzido do crédito na conta quando o domínio for renovado.
  {:note}
  
* Selecione o botão **Continuar** para transferir o domínio.

## Transferir vários domínios
{: #transfer-multiple-domains}

Os domínios poderão ser transferidos para o {{site.data.keyword.cloud_notm}} em massa a qualquer momento, em vez de individualmente, se houver um cartão de crédito ativo ou um crédito disponível na conta. Siga estas etapas para transferir múltiplos domínios para o {{site.data.keyword.cloud_notm}}.

* Navegue para a tela **Registro de domínio** no [{{site.data.keyword.cloud_notm}} Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). Consulte [Acessar a tela Registro de domínio](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen).
* Escolha a guia **Transferir**.
* Selecione a opção **Transferir múltiplos domínios?** na guia **Transferir**.
* Insira o nome de domínio existente no campo **Nome de domínio**.
* Selecione o tipo de domínio na lista suspensa de **Tipos de domínio**.
* Selecione a quantia de tempo durante a qual o domínio transferido permanecerá ativo na lista suspensa de **Tempos de registro**.

O preço para cada período de tempo é exibido ao lado do tempo e será cobrado no cartão de crédito ou deduzido do crédito na conta quando o domínio for renovado.
{:note}

* Repita para cada domínio adicional a ser transferido.

Selecione a opção **Incluir Outro** para preencher campos em branco adicionais para mais entradas de domínio. Selecione o ícone **Excluir** para excluir uma entrada inteira da tela.
{:note}

* Selecione o botão **Continuar** para transferir os domínios.



## O que acontece depois
{:#transfer-an-existing-domain-to-ibm-cloud-next}

Após você transferir um domínio, será possível gerenciá-lo dentro do [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Quando o registro do domínio se aproximar de sua data de expiração, ele poderá ser [renovado](/docs/infrastructure/dns?topic=dns-renew-an-existing-domain) na tela **Gerenciamento de domínio**.
