---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Gerenciar zonas de DNS secundárias
{: #manage-secondary-dns-zones}

O {{site.data.keyword.cloud}} fornece DNS secundário para todos os clientes como um meio de armazenar em cache Zonas de DNS primárias no evento de uma perda de dados. Não é obrigatório manter uma Zona de DNS secundária, mas é altamente recomendado para usuários com múltiplos domínios. 


## Incluir uma Zona de DNS secundária
{:#add-a-secondary-dns-zone}

Siga as etapas abaixo para incluir uma Zona de DNS secundária:

* Navegue para a tela **Zonas de DNS secundárias** no [{{site.data.keyword.cloud_notm}} Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) selecionando **Infraestrutura Clássica** no menu
de navegação. 
* Selecione **Rede > DNS > Zonas Secundárias** no menu de navegação Infraestrutura Clássica.
* Selecione a guia **Incluir zona**.
* Insira o **Domínio para a zona** no campo **Zona**.
* Insira o **Endereço IP do servidor de nomes principal** no campo **Servidor de nomes principal**.
* Insira o **tempo de transferência** (em minutos) durante o qual a Zona de DNS primária irá transferir para a Zona de DNS secundária no campo **Intervalo de transferência**.
* Selecione o botão **Incluir** para incluir a Zona ou selecione **Cancelar** para cancelar a ação.

### O que acontece após a inclusão
{:#add-a-secondary-dns-zone-next}

Após você criar uma Zona de DNS secundária, ela aparecerá na lista de Zonas na tela Zonas de DNS secundárias. A transferência de dados da Zona Primária para a Secundária ocorre em intervalos que você especifica quando a zona é criada. A qualquer momento, você pode [editar](#edit-a-secondary-dns-zone), [transferir manualmente](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) ou [converter](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) a Zona para uma Zona Primária. A Zona de DNS Secundária também pode ser [excluída](#delete-a-secondary-dns-zone) a qualquer momento.

## Edite uma Zona de DNS secundária
{:#edit-a-secondary-dns-zone}

As Zonas de DNS secundárias podem ser editadas a qualquer momento para atualizar o Servidor de nomes principal ou o Intervalo de transferência. Siga as etapas abaixo para editar uma Zona de DNS secundária.

* Navegue para a tela **Zonas de DNS secundárias** no [{{site.data.keyword.cloud_notm}} Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) selecionando **Infraestrutura Clássica** no menu
de navegação. 
* Selecione **Rede > DNS > Zonas Secundárias** no menu de navegação Infraestrutura Clássica.
* Clique em qualquer lugar na **linha que contém a Zona de DNS secundária** para abrir a Zona para edições.
  Se existirem diversas Zonas Secundárias, a visualização poderá ser filtrada para localizar a Zona que requer edições.
  {:note}  
* Atualize os campos **Servidor de nomes principal** e **Intervalo de transferência** conforme necessário.
* Selecione o botão **Atualizar** para atualizar a Zona de DNS secundária ou selecione **Cancelar** para cancelar a ação.

### O que acontece após a edição
{:#edit-a-secondary-dns-zone-next}

Após editar a Zona de DNS secundária, os valores **Servidor de nomes principal** e **Intervalo de transferência** refletirão a atualização e a Zona secundária começará a receber transferências com base nas informações novas. A qualquer momento, a Zona pode ser editada novamente repetindo as etapas acima.

## Excluir uma Zona de DNS secundária
{:#delete-a-secondary-dns-zone}

Após uma Zona de DNS secundária ter sido criada, ela poderá ser excluída a qualquer momento. Se uma Zona de DNS secundária for excluída, ela não poderá ser recuperada. Siga estas etapas para excluir um Registro de DNS secundária.

 * Navegue para a tela **Zonas de DNS secundárias** no [{{site.data.keyword.cloud_notm}} Console ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) selecionando **Infraestrutura Clássica** no menu
de navegação. 
* Selecione **Rede > DNS > Zonas Secundárias** no menu de navegação Infraestrutura Clássica.
* Selecione **Excluir** na lista suspensa de **Ações** para a Zona que requer exclusão. Uma caixa de confirmação pop-up aparecerá.
  Se existirem diversas Zonas secundárias, a visualização poderá ser filtrada para localizar a Zona para a exclusão.
  {:note}
* Selecione o botão **Sim** para confirmar a exclusão ou selecione o botão **Não** para cancelar a ação.

### O que acontece após a exclusão
{:#delete-a-secondary-dns-zone-next}

Após uma Zona de DNS secundária ser excluída, as transferências automáticas da Zona primária cessarão e o Zona secundária não existirá mais. Se uma Zona de DNS secundária for necessária para a Zona primária em qualquer momento, uma nova [Zona de DNS secundária poderá ser criada](#add-a-secondary-dns-zone).
