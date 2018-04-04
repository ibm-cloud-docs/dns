---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Effectuer un transfert de zone manuel pour une zone DNS secondaire 

En général, les transferts de zone DNS sont effectués automatiquement en fonction de l'intervalle de transfert DNS secondaire que vous avez spécifié. Vous pouvez utiliser un transfert de zone manuel pour forcer le transfert de contenu qui, faute de quoi, attendrait le prochain transfert automatique. Pour effectuer un transfert manuel,[vous devez établir une zone de DNS secondaire](add-secondary-dns-zone.html). Effectuez les étapes de cet article pour réalser un transfert de zone manuel pour un DNS secondaire. 

1. Accédez à l'écran de **Zones DNS secondaire** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/). Reportez-vous à la section [Utilisation de l'écran de zones DNS](delete-secondary-dns-record.html){:new_window}.
2. Sélectionnez **Forcer le transfert** dans la liste déroulante **Actions** pour commencer le transfert.

## Etapes suivantes

Une fois le transfert commencé, le statut passe à **Transfert en cours**. Les transferts manuels ne peuvent pas être annulés après leur lancement. Une fois les données transférées, les transferts de données reviennent à l'intervalle de transfert précédemment défini pour le DNS secondaire. Vous pouvez [modifier l'intervalle de transfert](edit-secondary-dns-zone.html) à tout moment pour éviter de devoir effectuer fréquemment des transferts de zone manuels.
