---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ajouter une zone DNS secondaire 

{{site.data.keyword.BluSoftlayer_notm}} fournit un DNS secondaire à tous les clients afin de mettre en cache les zones du DNS principal en cas de perte de données. Le maintien d'une zone DNS secondaire n'est pas obligatoire, mais il est vivement recommandé aux utilisateurs possédant plusieurs domaines. Effectuez les étapes ci-dessous pour ajouter une zone DNS secondaire : 

* Accédez à l'écran de **Zones DNS secondaire** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/).
Reportez-vous à la section [Utilisation de l'écran de zones DNS](use-dns-zones-screen.html){:new_window}.
* Sélectionnez l'onglet **Ajouter zone**.
* Entrez le **domaine de la zone** dans le champ **Zone**.
* Entrez l'**adresse IP du serveur de noms principal** dans le champ **Serveur de noms maître**. 
* Entrez la **durée de transfert (en minutes)** durant laquelle la zone DNS principale est transférée vers la zone DNS secondaire dans le champ d'**intervalle de transfert**. 
* Sélectionnez le bouton **Ajouter** pour ajouter la zone ou sélectionnez **Annuler** pour annuler l'action. 

## Etapes suivantes

Lorsqu'une zone DNS secondaire est créée, elle apparaît dans la liste des zones de l'écran Zones DNS secondaires. Le transfert des données de la zone principale vers la zone secondaire s'effectue à des intervalles que vous spécifiez lors de la création de la zone. A tout moment, vous pouvez [modifier](edit-secondary-dns-zone.html), [transférer manuellement](make-manual-zone-transfer-secondary-dns.html) ou [convertir](convert-secondary-dns-zone-primary-zone.html) la zone en zone principale. La zone DNS secondaire peut également être [supprimée](delete-secondary-dns-zone.html) à tout moment. 
