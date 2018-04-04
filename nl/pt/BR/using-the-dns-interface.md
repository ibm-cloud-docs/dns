---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Como usar a interface de DNS

Siga estas etapas para utilizar a interface de DNS através do portal do cliente do IBM Cloud:

* Navegue para o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/).
* Selecione **Rede->DNS->Encaminhar Zonas**
* Selecione o Domínio que deseja gerenciar ou selecione o botão **Incluir Zona de DNS** no lado direito da página.

## Visão geral da interface de DNS
Trabalhar na interface de DNS no Portal do cliente lhe dá recursos integrais para gerenciar todos os aspectos de seu DNS. É possível executar cada tipo de gerenciamento de DNS de qualquer tela na interface, usando a barra de menus estática na parte superior de sua tela.

## Gerenciar DNS
Após atingir a interface de DNS no Portal, você será encaminhado diretamente à tela **Gerenciar DNS**, que lhe permite visualizar, editar ou excluir qualquer DNS primário existente associado à sua conta.

* Para incluir novos registros simplesmente preencha os campos fornecidos sob **Incluir novo registro** e clique no botão **Incluir registro**.
* Para modificar um registro existente, clique na linha que contém o registro e ele será convertido para o modo **Editar**. Mude as configurações para os valores desejados e clique em **Atualizar**.
* Para excluir um registro, selecione o círculo vermelho à direita do registro e depois clique em **Sim** no prompt.

## DNS Secundário

* Navegue para o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/).
* Selecione **Rede->DNS->Zonas secundárias**

Nessa tela é possível incluir ou modificar as configurações de DNS secundárias.

* Para incluir um novo registro, selecione **Incluir zona**, preencha os campos e selecione **Incluir**.
* Para remover um registro de DNS secundário ou convertê-lo em um registro primário, use o menu suspenso **Ações** à direita da página e escolha a opção apropriada.

## DNS reverso

Siga estas etapas para utilizar a interface de DNS através da navegação do Portal:

* Navegue para o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/).
* Selecione **Rede->DNS->Registros reversos**
* No menu suspenso, selecione ou digite o endereço IP para o qual você deseja mudar o DNS reverso e, em seguida, selecione **Visualizar IP**
  * Para incluir o registro, insira o Nome do host que você deseja usar para a entrada de DNS reverso
  * Configure o TTL (Tempo de Vida) para o registro.
  * Quando você tiver certeza das informações, selecione **Salvar**.

É possível modificar uma sub-rede inteira clicando em **Editar RDNS para todos os IPs nessa sub-rede** à direita da página.

* Nessa página, selecione a linha para o IP que você deseja atualizar
* Digite as informações nos campos e, em seguida, selecione **Atualizar**. O campo "notas" é opcional.

## Verificação de propagação

* Navegue para o [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/).
* Selecione **Rede->Ferramentas**

Na página que é carregada, é possível selecionar dentre múltiplas ferramentas; para verificar a propagação de seu nome de domínio por meio dos servidores DNS, use a opção da parte inferior.

* Insira as informações apropriadas nos campos e, em seguida, selecione **Verificar DNS**
* Após alguns instantes, a caixa à direita será atualizada com as informações de DNS atual para o domínio.
