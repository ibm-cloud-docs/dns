---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Manual Zone Transfer, DNS Zone transfers, Secondary DNS Zone

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Effectuer un transfert de zone manuel pour une zone DNS secondaire
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

En général, les transferts de zone DNS sont effectués automatiquement en fonction de l'intervalle de transfert DNS secondaire que vous avez spécifié. Vous pouvez utiliser un transfert de zone manuel pour forcer le transfert de contenu qui, faute de quoi, attendrait le prochain transfert automatique. Pour effectuer un transfert manuel,[vous devez établir une zone de DNS secondaire](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone). Effectuez les étapes de cet article pour réaliser un transfert de zone manuel pour un DNS secondaire.

1. Accédez à l'écran de **Zones DNS secondaire** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). Reportez-vous à la section [Utilisation de l'écran de zones DNS](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window}.
2. Sélectionnez **Forcer le transfert** dans la liste déroulante **Actions** pour commencer le transfert.

## Etapes suivantes
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone-next}

Une fois le transfert commencé, le statut passe à **Transfert en cours**. Les transferts manuels ne peuvent pas être annulés après leur lancement. Une fois les données transférées, les transferts de données reviennent à l'intervalle de transfert précédemment défini pour le DNS secondaire. Vous pouvez [modifier l'intervalle de transfert](/docs/infrastructure/dns?topic=dns-edit-a-secondary-dns-zone) à tout moment pour éviter de devoir effectuer fréquemment des transferts de zone manuels.
