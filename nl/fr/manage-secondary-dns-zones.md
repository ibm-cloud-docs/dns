---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Gestion de zones DNS secondaires
{: #manage-secondary-dns-zones}

{{site.data.keyword.cloud}} fournit un DNS secondaire à tous les clients afin de mettre en cache les zones du DNS principal en cas de perte de données. Le maintien d'une zone DNS secondaire n'est pas obligatoire, mais il est vivement recommandé aux utilisateurs possédant plusieurs domaines. 


## Ajouter une zone DNS secondaire
{:#add-a-secondary-dns-zone}

Effectuez les étapes ci-dessous pour ajouter une zone DNS secondaire :

* Accédez à l'écran **Zones DNS secondaires** sur la [console {{site.data.keyword.cloud_notm}}![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS > Zones en amont** dans le menu de navigation Infrastructure classique.
* Sélectionnez l'onglet **Ajouter zone**.
* Entrez le **domaine de la zone** dans le champ **Zone**.
* Entrez l'**adresse IP du serveur de noms principal** dans le champ **Serveur de noms maître**.
* Entrez la **durée de transfert (en minutes)** durant laquelle la zone DNS principale est transférée vers la zone DNS secondaire dans le champ d'**intervalle de transfert**.
* Sélectionnez le bouton **Ajouter** pour ajouter la zone ou sélectionnez **Annuler** pour annuler l'action.

### Que se passe-t-il après l'ajout
{:#add-a-secondary-dns-zone-next}

Lorsqu'une zone DNS secondaire est créée, elle apparaît dans la liste des zones de l'écran Zones DNS secondaires. Le transfert des données de la zone principale vers la zone secondaire s'effectue à des intervalles que vous spécifiez lors de la création de la zone. A tout moment, vous pouvez [modifier](#edit-a-secondary-dns-zone), [transférer manuellement](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) ou [convertir](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) la zone en zone principale. La zone DNS secondaire peut également être [supprimée](#delete-a-secondary-dns-zone) à tout moment.

## Modifier une zone DNS secondaire
{:#edit-a-secondary-dns-zone}

Les zones DNS secondaires peuvent être modifiées à tout moment pour mettre à jour le serveur de noms maître ou l'intervalle de transfert. Effectuez les étapes ci-dessous pour modifier une zone DNS secondaire.

* Accédez à l'écran **Zones DNS secondaires** sur la [console {{site.data.keyword.cloud_notm}}![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS > Zones en amont** dans le menu de navigation Infrastructure classique.
* Cliquez n'importe où sur la **ligne contenant la zone DNS secondaire** pour ouvrir la zone pour les modifications.
  Si plusieurs zones secondaires existent, la vue peut être filtrée pour localiser la zone à modifier.
  {:note}  
* Mettez à jour les champs **Serveur de noms maître** et **Intervalle de transfert** si nécessaire.
* Sélectionnez le bouton **Mettre à jour** pour mettre à jour la zone DNS secondaire ou sélectionnez **Annuler** pour annuler l'action.

### Que se passe-t-il après la modification
{:#edit-a-secondary-dns-zone-next}

Après modification de la zone DNS secondaire, les valeurs **Serveur de noms maître** et **Intervalle de transfert** reflètent la mise à jour et la zone secondaire commence à recevoir des transferts basés sur les nouvelles informations. A tout moment, vous pouvez modifier la zone à nouveau en répétant les étapes ci-dessus.

## Supprimer une zone DNS secondaire
{:#delete-a-secondary-dns-zone}

Une fois qu'une zone DNS secondaire a été créée, elle peut être supprimée à tout moment. Sachez que si une zone DNS secondaire est supprimée, elle ne peut pas être récupérée. Effectuez les étapes ci-dessous pour supprimer un enregistrement DNS secondaire.

 * Accédez à l'écran **Zones DNS secondaires** sur la [console {{site.data.keyword.cloud_notm}}![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS > Zones en amont** dans le menu de navigation Infrastructure classique.
* Sélectionnez **Supprimer** dans la liste déroulante **Actions** pour la zone à supprimer. Une fenêtre contextuelle de confirmation apparaît.
  Si plusieurs zones secondaires existent, la vue peut être filtrée pour localiser la zone à supprimer.
  {:note}
* Sélectionnez le bouton **Oui** pour confirmer la suppression ou sélectionnez le bouton **Non** pour annuler l'action.

### Que se passe-t-il après la suppression
{:#delete-a-secondary-dns-zone-next}

Après la suppression d'une zone DNS secondaire, les transferts automatiques de la zone principale cessent et la zone secondaire n'existe plus. Si une zone DNS secondaire est requise à tout moment pour la zone principale, vous pouvez [créer une nouvelle DNS secondaire](#add-a-secondary-dns-zone).
