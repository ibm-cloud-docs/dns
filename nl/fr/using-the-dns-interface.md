---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Comment utiliser l'interface DNS

Effectuez les étapes ci-dessous pour utiliser l'interface DNS via le portail client IBM Cloud : 

* Accédez au [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/).
* Sélectionnez **Réseau->DNS->Zones en aval**
* Sélectionnez le domaine que vous souhaitez gérer ou sélectionnez le bouton **Ajouter zone DNS** sur le côté droit de la page. 

## Présentation de l'interface DNS 
L'utilisation de l'interface DNS sur le portail client vous offre toutes les possibilités pour gérer tous les aspects de votre DNS. Vous pouvez effectuer chaque type de gestion DNS à partir de n'importe quel écran de l'interface, à l'aide de la barre de menu statique en haut de votre écran. 

## Gérer le DNS 
En accédant à l'interface DNS du portail, vous êtes directement redirigé vers l'écran **Gérer DNS**, qui vous permet d'afficher, de modifier ou de supprimer tout DNS principal associé à votre compte. 

* Pour ajouter de nouveaux enregistrements, il vous suffit de remplir les champs fournis sous **Ajouter nouvel enregistrement** et de cliquer sur le bouton **Ajouter enregistrement**. 
* Pour modifier un enregistrement existant, cliquez sur la ligne contenant l'enregistrement afin de le faire passer en mode **édition**. Remplacez les paramètres par les valeurs souhaitées et cliquez sur **Mettre à jour**.
* Pour supprimer un enregistrement, sélectionnez le cercle rouge à droite de l'enregistrement, puis cliquez sur **Oui** à l'invite. 

## DNS Secondaire

* Accédez au [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/).
* Sélectionnez **Réseau->DNS->Zones secondaires**

A partir de cet écran, vous pouvez ajouter ou modifier les paramètres DNS secondaires. 

* Pour ajouter un nouvel enregistrement, sélectionnez **Ajouter une zone**, remplissez les champs et sélectionnez **Ajouter**. 
* Pour supprimer un enregistrement DNS secondaire ou le convertir en enregistrement principal, utilisez la liste déroulante **Actions** à droite de la page et sélectionnez l'option appropriée. 

## DNS en amont

Effectuez les étapes ci-dessous pour utiliser l'interface DNS via la navigation du portail :  

* Accédez au [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/).
* Sélectionnez **Réseau->DNS->Enregistrements en amont**
* Dans le menu déroulant, sélectionnez ou tapez l'adresse IP pour laquelle vous souhaitez modifier le DNS en amont, puis sélectionnez **Afficher IP**
  * Pour ajouter l'enregistrement, entrez le nom d'hôte que vous souhaitez utiliser pour l'entrée DNS en amont 
  * Définissez la Durée de vie de l'enregistrement. 
  * Lorsque vous êtes certain de l'information, sélectionnez **Sauvegarder**.

Vous pouvez modifier un sous-réseau entier en cliquant sur **Editer le RDNS pour toutes les adresses IP de ce sous-réseau** sur la droite de la page.

* A partir de cette page, sélectionnez la ligne de l'adresse IP que vous souhaitez mettre à jour 
* Entrez les informations dans les champs, puis sélectionnez **Mettre à jour**. Le champ "notes" est facultatif. 

## Vérification de la propagation

* Accédez au [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/).
* Sélectionnez **Réseau->Outils**

Sur la page du chargement, vous pouvez choisir parmi plusieurs outils ; pour vérifier la propagation de votre nom de domaine via les serveurs DNS, utilisez l'option du bas. 

* Entrez les informations appropriées dans les champs, puis sélectionnez **Vérifier DNS**
* Après quelques instants, la case de droite est mise à jour avec les informations DNS actuelles pour le domaine. 
