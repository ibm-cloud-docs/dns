---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Master Nameserver

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Edite uma Zona de DNS secundária
{:#edit-a-secondary-dns-zone}

As Zonas de DNS secundárias podem ser editadas a qualquer momento para atualizar o Servidor de nomes principal ou o Intervalo de transferência. Siga as etapas abaixo para editar uma Zona de DNS secundária.

* Navegue até a tela **Zonas Secundárias do DNS** no [Portal do Cliente![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) selecionando **Infraestrutura Clássica** no menu de navegação. 
* Selecione **Rede > DNS > Zonas Secundárias** no menu de navegação Infraestrutura Clássica.
* Clique em qualquer lugar na **linha que contém a Zona de DNS secundária** para abrir a Zona para edições.
  Se existirem diversas Zonas Secundárias, a visualização poderá ser filtrada para localizar a Zona que requer edições.
  {:note}  
* Atualize os campos **Servidor de nomes principal** e **Intervalo de transferência** conforme necessário.
* Selecione o botão **Atualizar** para atualizar a Zona de DNS secundária ou selecione **Cancelar** para cancelar a ação.

## O que acontece em seguida
{:#edit-a-secondary-dns-zone-next}

Após editar a Zona de DNS secundária, os valores **Servidor de nomes principal** e **Intervalo de transferência** refletirão a atualização e a Zona secundária começará a receber transferências com base nas informações novas. A qualquer momento, a Zona pode ser editada novamente repetindo as etapas acima.
