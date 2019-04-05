---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: create your own nameservers, cPanel, WHM

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Créer vos propres serveurs de noms dans cPanel/WHM
{:#create-your-own-nameservers-in-cpanel-whm}

Cet article explique comment créer vos propres serveurs de noms à l'aide du Gestionnaire WHM (Web Host Manager). Si vous rencontrez des problèmes après avoir effectué ces étapes, veuillez soumettre un ticket de demande de service faisant référence à cet article.

1. Décidez d'abord quels seront les noms de vos serveurs de noms. Supposons que votre société d'hébergement s'appelle "Awesome Server Hosting" et que vous souhaitiez configurer `ns1.awesomeserverhosting.com` et `ns2.awesomeserverhosting.com`.

* Connectez-vous à WHM sur votre serveur en accédant à `https://XX.XX.XX.XX:2087` dans votre navigateur.

* Pour configurer vos serveurs de noms, sélectionnez la première option dans la barre de gauche, qui doit être "Basic cPanel/WHM Setup". 

 * Ici vous pouvez définir le nom de vos serveurs de noms principaux, secondaires, tertiaires et quaternaires.

 * Lorsque vous avez terminé, sélectionnez le bouton "Save".

2. A présent, créez le fichier Zone pour `awesomeserverhosting.com` dans votre serveur. Vous pouvez effectuer cette tâche de deux manières :

Première méthode : créez le compte de domaine pour "awesomeserverhosting.com". Les instructions de cette opération dépassent la portée de cet article, veuillez consulter la [documentation cPanel](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html) pour plus d'informations : 

   * Sélectionnez "Ajouter une zone DNS" sous "Fonctions DNS" dans la barre latérale gauche.

   * Entrez l'adresse IP d'hébergement du site Web principal pour `awesomeserverhosting.com` et bien sûr, le nom de domaine.

   **Remarque : effectuez cette tâche uniquement si vous ne prévoyez pas l'hébergement de `awesomeserverhosting.com` sur ce serveur !**

   * Sous la rubrique **Networking Setup**, cliquez sur **Nameserver IPs**.

   * Fournissez les noms de vos serveurs de noms. Par exemple, soumettez `ns1.awesomeserverhosting.com` et `ns2.awesomeserverhosting.com`.

   * Dans la barre de gauche, recherchez **Nameserver Setup** sous **Service Configuration**.

   * Un message similaire à celui-ci s'affichera : "We recommend you do not enable the nameserver unless you are going to use it. If you wish to disable the nameserver you can always turn it off in the Service Manager".

   * Vous allez à présent mettre en service vos serveurs de noms, pour cela sélectionnez le bouton **Proceed >>**. L'outil `cPanel` vérifie que les packages appropriés sont installés sur votre serveur et qu'ils sont configurés et fonctionnent correctement pour héberger vos services de nom de domaine. Vous êtes prêt !

Liens externes :

* [Documentation cPanel](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
