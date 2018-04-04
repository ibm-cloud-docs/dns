---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Incluir uma Zona de DNS secundária

O {{site.data.keyword.BluSoftlayer_notm}} fornece DNS secundário para todos os clientes como um meio de armazenar em cache Zonas de DNS primárias no evento de uma perda de dados. Não é obrigatório manter uma Zona de DNS secundária, mas é altamente recomendado para usuários com múltiplos domínios. Siga as etapas abaixo para incluir uma Zona de DNS secundária:

* Navegue para a tela **Zonas do DNS secundárias** no [Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/). Consulte [Usando a tela Zonas do DNS](use-dns-zones-screen.html){:new_window}.
* Selecione a guia **Incluir zona**.
* Insira o **Domínio para a zona** no campo **Zona**.
* Insira o **Endereço IP do servidor de nomes principal** no campo **Servidor de nomes principal**.
* Insira o **tempo de transferência** (em minutos) durante o qual a Zona de DNS primária irá transferir para a Zona de DNS secundária no campo **Intervalo de transferência**.
* Selecione o botão **Incluir** para incluir a Zona ou selecione **Cancelar** para cancelar a ação.

## O que acontece em seguida

Após você criar uma Zona de DNS secundária, ela aparecerá na lista de Zonas na tela Zonas de DNS secundárias. A transferência de dados da Zona Primária para a Secundária ocorre em intervalos que você especifica quando a zona é criada. A qualquer momento, você pode [editar](edit-secondary-dns-zone.html), [transferir manualmente](make-manual-zone-transfer-secondary-dns.html) ou [converter](convert-secondary-dns-zone-primary-zone.html) a Zona para uma Zona Primária. A Zona de DNS Secundária também pode ser [excluída](delete-secondary-dns-zone.html) a qualquer momento.
