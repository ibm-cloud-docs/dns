---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, IBM Cloud, Add Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Incluir uma Zona de DNS secundária
{:#add-a-secondary-dns-zone}

O {{site.data.keyword.BluSoftlayer_notm}} fornece DNS secundário para todos os clientes como um meio de armazenar em cache Zonas de DNS primárias no evento de uma perda de dados. Não é obrigatório manter uma Zona de DNS secundária, mas é altamente recomendado para usuários com múltiplos domínios. Siga as etapas abaixo para incluir uma Zona de DNS secundária:

* Navegue até a tela **Zonas Secundárias do DNS** no [Portal do Cliente![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) selecionando **Infraestrutura Clássica** no menu de navegação. 
* Selecione **Rede > DNS > Zonas Secundárias** no menu de navegação Infraestrutura Clássica.
* Selecione a guia **Incluir zona**.
* Insira o **Domínio para a zona** no campo **Zona**.
* Insira o **Endereço IP do servidor de nomes principal** no campo **Servidor de nomes principal**.
* Insira o **tempo de transferência** (em minutos) durante o qual a Zona de DNS primária irá transferir para a Zona de DNS secundária no campo **Intervalo de transferência**.
* Selecione o botão **Incluir** para incluir a Zona ou selecione **Cancelar** para cancelar a ação.

## O que acontece em seguida
{:#add-a-secondary-dns-zone-next}

Após você criar uma Zona de DNS secundária, ela aparecerá na lista de Zonas na tela Zonas de DNS secundárias. A transferência de dados da Zona Primária para a Secundária ocorre em intervalos que você especifica quando a zona é criada. A qualquer momento, você pode [editar](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record), [transferir manualmente](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) ou [converter](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) a Zona para uma Zona Primária. A Zona de DNS Secundária também pode ser [excluída](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone) a qualquer momento.
