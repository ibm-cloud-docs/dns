---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Converter uma Zona de DNS secundária em uma Zona primária
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

A qualquer momento, uma [Zona de DNS secundária](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window} pode ser convertida em sua Zona primária. Quando você converte uma Zona de DNS secundária em primária, os servidores de nomes do {{site.data.keyword.BluSoftlayer_notm}} se tornam os servidores de nomes autorizados para a Zona convertida. Siga as etapas abaixo para converter uma Zona de DNS secundária em primária:

* Navegue até a tela **Zonas Secundárias do DNS** no [Portal do Cliente![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) selecionando **Infraestrutura Clássica** no menu de navegação. 
* Selecione **Rede > DNS > Zonas Secundárias** no menu de navegação Infraestrutura Clássica.
* Selecione **Converter em primária** na lista suspensa **Ações** para a Zona secundária desejada.
* Selecione o botão **Sim** para converter a Zona ou selecione **Não** para cancelar a ação.

## O que acontece em seguida
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

Após você converter a Zona de DNS secundária em primária, será possível visualizá-la na tela **Encaminhar zonas**. Todos os registros de SOA e de NS que existiam anteriormente para a Zona serão substituídos por registros de SOA e de NS do {{site.data.keyword.BluSoftlayer_notm}}, que não podem ser editados. Você ainda pode [editar outros registros de Zona](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record).
