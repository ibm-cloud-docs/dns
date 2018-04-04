---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ajouter une zone DNS 

La gestion DNS par {{site.data.keyword.BluSoftlayer_notm}} s'étend aux zones DNS qui ne se trouvent peut-être pas sur le réseau {{site.data.keyword.BluSoftlayer_notm}}. A l'aide de l'interface, vous pouvez ajouter des zones DNS à tout moment, en tant que domaine unique ou en masse. L'ajout de zones DNS a actuellement lieu dans la version [Contrôle](https://control.softlayer.com/) du portail client. Effectuez les étapes ci-dessous pour ajouter une ou plusieurs zones DNS. 

* Connectez-vous à la version [Contrôle](https://control.softlayer.com/) du portail client à l'aide de vos identifiants uniques.
* Sélectionnez **DNS** dans le menu déroulant **Réseau**.
* Sélectionnez **Zones en aval**.
* Sélectionnez l'onglet **Ajouter zone DNS** en haut à droite.
* Déterminez si vous ajoutez un seul domaine ou plusieurs domaines :<br> <br><table border="1"><tbody><tr><th>Si vous ajoutez...</th><th>Alors...</th></tr><tr><td>Un seul domaine</td><td>Complétez les étapes suivantes dans la section <strong>Ajouter un seul domaine</strong> de l'écran :<br> <ul><li>Entrez le <strong>nom de domaine</strong> dans le champ <strong>Nom du domaine</strong>.</li><li>Entrez l'<strong>adresse IP</strong> vers laquelle le nom de domaine pointe dans le champ <strong>Adresse IP</strong>. </li><li>Cliquez sur le bouton <strong>Ajouter une zone</strong> pour ajouter le domaine. <br> </li></ul></td></tr><tr><td>Domaines multiples</td><td>Déterminez si les domaines sont associés à une adresse IP unique ou à plusieurs adresses IP : <br> <p> </p><p> </p><p> </p><p> </p><ul><li>Si les domaines sont associés à une seule adresse IP,<ul><li>Entrez <strong>chaque domaine</strong> dans la zone de texte <strong>Domaines</strong>. </li><li>Entrez l'<strong>adresse IP</strong> dans le champ <strong>Adresse IP par défaut</strong>. </li><li>Cliquez sur le bouton <strong>Ajouter zone</strong> pour ajouter les domaines en masse.</li></ul></li><li>Si les domaines sont associés à plusieurs adresses IP,<ul><li>Entrez <strong>chaque domaine</strong> et son <strong>adresse IP</strong> correspondante en tant qu'élément de ligne unique dans la zone de texte <strong>Domaines</strong>. </li><li>Cliquez sur le bouton <strong>Ajouter zone</strong> pour ajouter les domaines en masse.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## Etapes suivantes

Lorsqu'une zone DNS est ajoutée, elle apparaît dans la liste des zones DNS sur l'[écran de Zones DNS](access-dns-zones-screen.html) dans le [portail client![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/). La zone peut être [modifiée](edit-dns-zone-record.html) ou [supprimée](delete-dns-zone.html) à tout moment. 
