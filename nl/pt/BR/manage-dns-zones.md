---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Gerenciar zonas de DNS
{: #manage-dns-zones}

## Incluir uma Zona de DNS
{: #add-a-dns-zone}

O gerenciamento de DNS pelo {{site.data.keyword.cloud}} se estende a Zonas de DNS que podem não estar na rede do {{site.data.keyword.cloud_notm}}. Usando a nossa interface, você pode incluir Zonas de DNS a qualquer momento, como um domínio único ou em massa. A adição de Zonas de DNS atualmente ocorre
no [IBM Cloud Console](https://{DomainName}/). Siga as etapas abaixo para incluir
uma ou mais Zonas de DNS.

* Efetue login no [IBM Cloud Console](https://{DomainName}/) usando suas
credenciais exclusivas.
* Selecione **Infraestrutura clássica** no Menu de Navegação
* Selecione **DNS** no menu suspenso **Rede**.
* Selecione **Encaminhar zonas**.
* Selecione a guia **Incluir Zona de DNS** na parte superior direita.
* Determine se você está incluindo um único domínio ou múltiplos domínios:

|Se estiver incluindo...|Então...|
|---|---|
|Um único domínio| Conclua as etapas a seguir na seção **Incluir domínio único** da tela: <ul><li>Insira o **Nome de domínio** no campo **Nome de domínio**.</li><li>Insira o **Endereço IP** para o qual o nome de domínio apontará no campo **Endereço IP**.</li><li>Clique no botão **Incluir zona** para incluir o domínio.</li></ul>|
|Múltiplos domínios| Determine se os domínios serão associados a um único endereço IP ou a múltiplos IPs: <ul><li>Se domínios forem associadas a um único endereço IP, <ul><li>insira **cada domínio** na caixa de texto **Domínios**.</li><li>Insira o **Endereço IP** no campo **Endereço IP padrão**.</li><li>Clique no botão **Incluir zona** para incluir os domínios em massa.</li></ul></li><li>Se domínios forem associados a múltiplos endereços IP, <ul><li>insira **cada domínio** e seu **Endereço IP** correspondente
como um único item de linha na caixa de texto **Domínios**.</li><li>Clique no botão **Incluir zona** para incluir os domínios em massa.</li></ul></li></ul>


### O que acontece em seguida
{:#add-a-dns-zone-next}

Depois de incluir uma zona única com sucesso, você será redirecionado automaticamente
para a página Edição de zona. Novas Zonas de DNS aparecerão na lista de Zonas de DNS na [tela Zonas de DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)
dentro do [IBM Cloud Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). A Zona pode ser [editada](#edit-a-dns-zone) ou [excluída](#delete-a-dns-zone) a qualquer momento.

## Editar uma Zona de DNS
{: edit-a-dns-zone}
Selecione a Zona de DNS que você deseja editar na lista de zonas na tela Zonas de DNS clicando
no nome da zona. Isso abre a página Zona de edição de DNS. Aqui, é possível fazer mudanças na Zona de DNS e clicar em **Atualizar SOA** para confirmar as mudanças. 

A tela **Editar uma Zona de DNS** permite incluir novos registros e
editar os registros existentes para a zona que você está editando. Também é possível exportar
ou excluir a zona nessa tela.

### O que acontece em seguida
{:#edit-a-dns-zone-next}

Clique em **Visualizar todas as Zonas de DNS** para retornar à lista
de Zonas de DNS.


## Excluir uma Zona de DNS
{: #delete-a-dns-zone}

Após uma Zona de DNS ter sido incluída, ela poderá excluída a qualquer momento. As exclusões de Zona de DNS são permanentes; elas não podem ser desfeitas. Siga estas etapas para excluir uma Zona de DNS:

* Navegue até a tela **Zona do DNS** desejada selecionando **Infraestrutura Clássica** no menu de navegação. 
* Selecione **Rede > DNS** no menu de navegação Infraestrutura Clássica
e escolha o tipo de zona que você precisa.
* Selecione o ícone **Excluir** no término da linha que contém a Zona de DNS desejada. Uma caixa de confirmação pop-up aparecerá.
* Selecione o botão **Sim** para confirmar a exclusão ou selecione o botão **Não** para cancelar a ação.

As zonas também podem ser excluídas de dentro da tela Editar Zonas de DNS.
{:tip}

### O que acontece em seguida
{:#delete-a-dns-zone-next}

Após a exclusão de uma Zona de DNS, ela não poderá mais ser gerenciada usando o [IBM Cloud Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/). Para novamente gerenciar uma zona excluída no Painel, ela deve ser [incluída como uma nova Zona](#add-a-dns-zone).
