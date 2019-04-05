---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Select Basic cPanel, Private Nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Créer des serveurs de noms privés dans cPanel/WHM
{:#create-private-nameservers-in-cpanel-whm}

A l'aide du produit cPanel/WHM, vous pouvez créer des serveurs de noms privés à tout moment. Les serveurs de noms privés permettent aux serveurs de noms associés à un site Web (par exemple `www.yourdomain.com`) d'afficher le serveur de noms du site Web (par exemple, `ns1.yourdomain.com`) à la place du serveur de noms associé à l'hôte du site Web (par exemple `ns1.webhostdomain.com`). L'ajout d'un serveur de noms privé à un domaine entraîne également l'affichage des options supplémentaires pour la gestion DNS dans cPanel/WHM. Effectuez les étapes de cet article pour créer un serveur de noms privé. Si des problèmes surviennent pendant ou après l'exécution de cette procédure, [ouvrez un ticket](/docs/get-support?topic=get-support-getting-customer-support).

## Attribuer un nom au serveur de noms
{:#name-the-nameserver}

* Connectez-vous à WHM sur votre serveur à l'adresse URL suivante : `http://xx.xx.xx.xx:2086`.
* Sélectionnez **Basic cPanel/WHM Setup** dans le menu **Server Configuration**.
* Entrez le ou les noms d'hôte du serveur de noms souhaité dans un ou plusieurs des champs suivants :
  * Serveur de noms principal
  * Serveur de noms secondaire
  * Serveur de noms tertiaire
  * Serveur de noms quaternaire
* Sélectionnez le bouton **Save**.

## Créer un fichier de zone pour le domaine
{:#create-a-zone-file-for-the-domain}

* Sélectionnez **Ajouter une zone DNS** dans le menu des **fonctions DNS**.
* Entrez l'**adresse IP** du domaine dans le champ de l'**adresse IP**.
* Entrez le **nom de domaine** dans le champ de **domaine**.

Vous pouvez également créer un compte de domaine en utilisant la procédure [Créer un compte](https://docs.cpanel.net/display/70Docs/Create+a+New+Account) décrite dans la documentation WHM de cPanel.
{:note}

## Attribuer une adresse IP au serveur de noms
{:#assign-an-ip-to-the-nameserver}

* Sélectionnez **Nameserver IPs** dans le menu **Network Setup**.
* Entrez le nom du premier **serveur de noms** dans le champ **Nameserver**.
* Cliquez sur le bouton **Assign**.
* Répétez les étapes ci-dessus pour chaque serveur de noms.

## Configurer le serveur de noms
{:#setup-the-nameserver}

* Sélectionnez **Nameserver Setup** dans le menu **Service Configuration**.
* Sélectionnez le bouton **Proceed** dans le message contextuel.
