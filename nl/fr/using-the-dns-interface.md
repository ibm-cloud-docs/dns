---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Comment utiliser l'interface DNS
{:#how-to-use-the-dns-interface}

Effectuez les étapes ci-dessous pour utiliser l'interface DNS via le portail client IBM Cloud :

* Accédez au [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/).
* Sélectionnez **Infrastructure classique** dans le menu de navigation
* Sélectionnez **Réseau->DNS->Zones en aval**
* Sélectionnez le domaine que vous souhaitez gérer ou sélectionnez le bouton **Ajouter zone DNS** sur le côté droit de la page.

## Présentation de l'interface DNS
{:#dns-interface-overview}
L'utilisation de l'interface DNS sur le portail client vous offre toutes les possibilités pour gérer tous les aspects de votre DNS. Vous pouvez effectuer chaque type de gestion DNS à partir de n'importe quel écran de l'interface, à l'aide de la barre de menu statique en haut de votre écran.

## Gérer le DNS
{:#manage-dns}
En accédant à l'interface DNS du portail, vous êtes directement redirigé vers l'écran **Gérer DNS**, qui vous permet d'afficher, de modifier ou de supprimer tout DNS principal associé à votre compte.

* Pour ajouter de nouveaux enregistrements, il vous suffit de remplir les champs fournis sous **Ajouter nouvel enregistrement** et de cliquer sur le bouton **Ajouter enregistrement**.
* Pour modifier un enregistrement existant, cliquez sur la ligne contenant l'enregistrement afin de le faire passer en mode **édition**. Remplacez les paramètres par les valeurs souhaitées et cliquez sur **Mettre à jour**.
* Pour supprimer un enregistrement, sélectionnez le cercle rouge à droite de l'enregistrement, puis cliquez sur **Oui** à l'invite.

## DNS Secondaire
{:#secondary-dns}

* Accédez à l'[Infrastructure classique du portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/).
* Sélectionnez **Infrastructure classique** dans le menu de navigation
* Sélectionnez **Réseau->DNS->Zones secondaires**

A partir de cet écran, vous pouvez ajouter ou modifier les paramètres DNS secondaires.

* Pour ajouter un nouvel enregistrement, sélectionnez **Ajouter une zone**, remplissez les champs et sélectionnez **Ajouter**.
* Pour supprimer un enregistrement DNS secondaire ou le convertir en enregistrement principal, utilisez la liste déroulante **Actions** à droite de la page et sélectionnez l'option appropriée.

## DNS en amont
{:#reverse-dns}

Effectuez les étapes ci-dessous pour utiliser l'interface DNS via la navigation du portail :

* Accédez à l'[Infrastructure classique du portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/).
* Sélectionnez **Infrastructure classique** dans le menu de navigation
* Sélectionnez **Réseau->DNS->Enregistrements en amont**
* Dans le menu déroulant, sélectionnez ou tapez l'adresse IP pour laquelle vous souhaitez modifier le DNS en amont, puis sélectionnez **Afficher IP**
  * Pour ajouter l'enregistrement, entrez le nom d'hôte que vous souhaitez utiliser pour l'entrée DNS en amont
  * Définissez la Durée de vie de l'enregistrement.
  * Lorsque vous êtes certain de l'information, sélectionnez **Sauvegarder**.

Vous pouvez modifier un sous-réseau entier en cliquant sur **Editer le RDNS pour toutes les adresses IP de ce sous-réseau** sur la droite de la page.

* A partir de cette page, sélectionnez la ligne de l'adresse IP que vous souhaitez mettre à jour
* Entrez les informations dans les champs, puis sélectionnez **Mettre à jour**. Le champ "notes" est facultatif.

<!--## Propagation Check

* Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network > Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
