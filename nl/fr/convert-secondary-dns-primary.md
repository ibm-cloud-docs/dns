---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Convertir une zone DNS secondaire en une zone principale 

A tout moment, une [zone DNS secondaire](add-secondary-dns-zone.html){:new_window} peut être convertie en zone principale. Lorsque vous convertissez une zone DNS secondaire en zone principale, les serveurs de noms {{site.data.keyword.BluSoftlayer_notm}} deviennent les serveurs de noms faisant autorité pour la zone convertie. Effectuez les étapes ci-dessous pour convertir une zone DNS secondaire en zone principale : 

* Accédez à l'écran de **Zones DNS secondaire** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/). Reportez-vous à la section [Utilisation de l'écran de zones DNS](use-dns-zones-screen.html){:new_window}.
* Sélectionnez **Convertir en zone principale** dans la liste déroulante **Actions** correspondant à la zone secondaire souhaitée.
* Sélectionnez le bouton **Oui** pour convertir la zone ou sélectionnez **Non** pour annuler l'action. 

## Etapes suivantes

Après avoir converti la zone DNS secondaire en zone principale, vous pouvez l'afficher dans l'écran **Zones en aval**. Tous les enregistrements SOA et NS qui existaient auparavant pour la zone sont remplacés par les enregistrements SOA et NS {{site.data.keyword.BluSoftlayer_notm}} qui ne peuvent pas être modifiés. Vous pouvez toujours [modifier les enregistrements de zone restants](edit-dns-zone-record.html).
