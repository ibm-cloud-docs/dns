---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Converter uma Zona de DNS secundária em uma Zona primária

A qualquer momento, uma [Zona de DNS secundária](add-secondary-dns-zone.html){:new_window} pode ser convertida em sua Zona primária. Quando você converte uma Zona de DNS secundária em primária, os servidores de nomes do {{site.data.keyword.BluSoftlayer_notm}} se tornam os servidores de nomes autorizados para a Zona convertida. Siga as etapas abaixo para converter uma Zona de DNS secundária em primária:

* Navegue para a tela **Zonas do DNS secundárias** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Consulte [Usando a tela Zonas do DNS](use-dns-zones-screen.html){:new_window}.
* Selecione **Converter em primária** na lista suspensa **Ações** para a Zona secundária desejada.
* Selecione o botão **Sim** para converter a Zona ou selecione **Não** para cancelar a ação.

## O que acontece em seguida

Após você converter a Zona de DNS secundária em primária, será possível visualizá-la na tela **Encaminhar zonas**. Todos os registros de SOA e de NS que existiam anteriormente para a Zona serão substituídos por registros de SOA e de NS do {{site.data.keyword.BluSoftlayer_notm}}, que não podem ser editados. Você ainda pode [editar outros registros de Zona](edit-dns-zone-record.html).
