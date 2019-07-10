---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-06-11"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Como usar a interface de DNS
{:#how-to-use-the-dns-interface}

Siga estas etapas para utilizar a interface de DNS por meio do portal do cliente de
infraestrutura do {{site.data.keyword.cloud}}:

* Navegue para o [portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/).
* Selecione **Infraestrutura clássica** no Menu de Navegação
* Selecione **Rede->DNS->Encaminhar Zonas**
* Selecione o Domínio que deseja gerenciar ou selecione o botão **Incluir Zona de DNS** no lado direito da página.

## Visão geral da interface de DNS
{:#dns-interface-overview}
Trabalhar na Interface de DNS no portal do cliente fornece recursos integrais para gerenciar todos
os aspectos de seu DNS. É possível executar cada tipo de gerenciamento de DNS de qualquer tela na interface, usando a barra de menus estática na parte superior de sua tela.

## Gerenciar DNS
{:#manage-dns}
Após atingir a interface de DNS no Portal, você será encaminhado diretamente à tela **Gerenciar DNS**, que lhe permite visualizar, editar ou excluir qualquer DNS primário existente associado à sua conta.

* Para incluir novos registros simplesmente preencha os campos fornecidos sob **Incluir novo registro** e clique no botão **Incluir registro**.
* Para modificar um registro existente, clique na linha que contém o registro e ele será convertido para o modo **Editar**. Mude as configurações para os valores desejados e clique em **Atualizar**.
* Para excluir um registro, selecione o círculo vermelho à direita do registro e depois clique em **Sim** no prompt.

## DNS Secundário
{:#secondary-dns}

* Navegue para o [portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/).
* Selecione **Infraestrutura clássica** no Menu de Navegação
* Selecione **Rede->DNS->Zonas secundárias**

Nessa tela é possível incluir ou modificar as configurações de DNS secundárias.

* Para incluir um novo registro, selecione **Incluir zona**, preencha os campos e selecione **Incluir**.
* Para remover um registro de DNS secundário ou convertê-lo em um registro primário, use o menu suspenso **Ações** à direita da página e escolha a opção apropriada.

## DNS reverso
{:#reverse-dns}

Siga estas etapas para utilizar a interface de DNS através da navegação do Portal:

* Navegue para o [portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/).
* Selecione **Infraestrutura clássica** no Menu de Navegação
* Selecione **Rede->DNS->Registros reversos**
* No menu suspenso, selecione ou digite o endereço IP para o qual você deseja mudar o DNS reverso e, em seguida, selecione **Visualizar IP**
  * Para incluir o registro, insira o Nome do host que você deseja usar para a entrada de DNS reverso
  * Configure o TTL (Tempo de Vida) para o registro.
  * Quando você tiver certeza das informações, selecione **Salvar**.

É possível modificar uma sub-rede inteira clicando em **Editar RDNS para todos os IPs nessa sub-rede** à direita da página.

* Nessa página, selecione a linha para o IP que você deseja atualizar
* Digite as informações nos campos e, em seguida, selecione **Atualizar**. O campo "notas" é opcional.

<!--## Propagation Check

* Navigate to the [customer portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network >Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
