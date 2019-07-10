---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Gestion des zones DNS
{: #manage-dns-zones}

## Ajouter une zone DNS
{: #add-a-dns-zone}

La gestion DNS par {{site.data.keyword.cloud}} s'étend aux zones DNS qui ne se trouvent peut-être pas sur le réseau {{site.data.keyword.cloud_notm}}. A l'aide de l'interface, vous pouvez ajouter des zones DNS à tout moment, en tant que domaine unique ou en masse. L'ajout de zones DNS a actuellement lieu dans la [console IBM Cloud](https://{DomainName}/). Effectuez les étapes ci-dessous pour ajouter une ou plusieurs zones DNS.

* Connectez-vous à la [Console IBM Cloud](https://{DomainName}/) à l'aide de vos identifiants uniques. 
* Sélectionnez **Infrastructure classique** dans le menu de navigation
* Sélectionnez **DNS** dans le menu déroulant **Réseau**.
* Sélectionnez **Zones en aval**.
* Sélectionnez l'onglet **Ajouter zone DNS** en haut à droite.
* Déterminez si vous ajoutez un seul domaine ou plusieurs domaines :

|Si vous ajoutez...|Alors...|
|---|---|
|Un seul domaine| Complétez les étapes suivantes dans la section **Ajouter un seul domaine** de l'écran : <ul><li>Entrez le **nom de domaine** dans le champ **Nom du domaine**.</li><li>Entrez l'**adresse IP** vers laquelle le nom de domaine pointe dans le champ **Adresse IP**.</li><li>Cliquez sur le bouton **Ajouter une zone** pour ajouter le domaine.</li></ul>|
|Domaines multiples| Déterminez si les domaines sont associés à une adresse IP unique ou à plusieurs adresses IP : <ul><li>Si les domaines sont associés à une seule adresse IP, <ul><li>Entrez **chaque domaine** dans la zone de texte **Domaines**.</li><li>Entrez l'**adresse IP** dans le champ **Adresse IP par défaut**.</li><li>Cliquez sur le bouton **Ajouter zone** pour ajouter les domaines en masse.</li></ul></li><li>Si les domaines sont associés à plusieurs adresses IP, <ul><li>Entrez **chaque domaine** et son **adresse IP** correspondante en tant qu'élément de ligne unique dans la zone de texte **Domaines**.</li><li>Cliquez sur le bouton **Ajouter zone** pour ajouter les domaines en masse.</li></ul></li></ul>


### Etapes suivantes
{:#add-a-dns-zone-next}

Après l'ajout d'une zone, vous serez redirigé vers la page d'édition de la zone.
De nouvelles zones DNS apparaissent dans la liste des zones DNS sur l'[écran de Zones DNS](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) sur la [console IBM Cloud ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). La zone peut être [modifiée](#edit-a-dns-zone) ou [supprimée](#delete-a-dns-zone) à tout moment.

## Modifier zone DNS
{: edit-a-dns-zone}
Sélectionnez la zone DNS que vous voulez modifier dans la liste des zones de l'écran Zones DNS en cliquant sur le nom de cette zone. La page Zone de modification DNS s'affiche. Vous pouvez alors apporter des modifications à la zone DNS, puis cliquer sur **Mettre à jour SOA** pour valider les modifications. 

Dans l'écran **Modifier une zone DNS**, vous pouvez ajouter des enregistrements et modifier des enregistrements existants pour la zone en cours de modification. Vous pouvez également exporter ou supprimer la zone depuis cet écran.

### Etapes suivantes
{:#edit-a-dns-zone-next}

Cliquez sur **Afficher toutes les zones DNS** pour revenir à la liste des zones DNS.


## Supprimer une zone DNS
{: #delete-a-dns-zone}

Une fois qu'une zone DNS a été ajoutée, vous pouvez la supprimer à tout moment. Les suppressions de zones DNS sont permanentes et irréversibles. Effectuez ces étapes pour supprimer une zone DNS :

* Accédez à l'écran **Zones DNS** désiré en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS** dans le menu de navigation Infrastructure classique et choisissez le type de zone dont vous avez besoin.
* Sélectionnez l'icône **Supprimer** à la fin de la ligne contenant la zone DNS souhaitée. Une fenêtre contextuelle de confirmation apparaît.
* Sélectionnez le bouton **Oui** pour confirmer la suppression ou sélectionnez le bouton **Non** pour annuler l'action.

Il est également possible de supprimer des zones depuis l'écran Modifier des zones DNS.
{:tip}

### Etapes suivantes
{:#delete-a-dns-zone-next}

Après la suppression d'une zone DNS, vous ne pouvez plus la gérer à l'aide de la [console IBM Cloud![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). Pour gérer à nouveau la zone supprimée dans le tableau de bord, vous devez l'[ajouter en tant que nouvelle zone](#add-a-dns-zone).
