---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Excluir uma Zona de DNS secundária
{:#delete-a-secondary-dns-zone}

Após uma Zona de DNS secundária ter sido criada, ela poderá ser excluída a qualquer momento. Se uma Zona de DNS secundária for excluída, ela não poderá ser recuperada. Siga as etapas abaixo para excluir um Registro de DNS secundário.

 * Navegue até a tela **Zonas Secundárias do DNS** no [Portal do Cliente![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/) selecionando **Infraestrutura Clássica** no menu de navegação. 
* Selecione **Rede > DNS > Zonas Secundárias** no menu de navegação Infraestrutura Clássica.
* Selecione **Excluir** na lista suspensa de **Ações** para a Zona que requer exclusão. Uma caixa de confirmação pop-up aparecerá.
  Se existirem diversas Zonas secundárias, a visualização poderá ser filtrada para localizar a Zona para a exclusão.
  {:note}
* Selecione o botão **Sim** para confirmar a exclusão ou selecione o botão **Não** para cancelar a ação.

## O que acontece em seguida
{:#delete-a-secondary-dns-zone-next}

Após uma Zona de DNS secundária ser excluída, as transferências automáticas da Zona primária cessarão e o Zona secundária não existirá mais. Se uma Zona de DNS secundária for necessária para a Zona primária em qualquer momento, uma nova [Zona de DNS secundária poderá ser criada](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone).
