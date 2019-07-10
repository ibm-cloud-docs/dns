---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Disable Recursion, DNS IBM Cloud DNS servers, BIND configuration file

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Désactiver la récursivité pour DNS
{:#disable-recursion-for-dns}

Les serveurs DNS IBM Cloud effectuent la récursivité par défaut La récursivité permet à votre serveur DNS de contacter d'autres serveurs DNS pour aider à résoudre les noms de domaine lorsqu'il ne peut pas résoudre le domaine lui-même. La récursivité peut s'avérer utile lorsqu'elle est nécessaire. Cependant, elle expose également le serveur DNS aux attaques, ce qui peut complètement détruire le serveur DNS. Les administrateurs système identifient généralement un besoin de récursivité et agissent en conséquence. Si tel n'est pas le cas, il est préférable de désactiver la récursivité. Effectuez les étapes ci-dessous en fonction de votre système d'exploitation ou de votre panneau de contrôle pour désactiver la récursivité DNS.

## Désactiver la récursivité dans Plesk
{:#disable-recursion-in-plesk}
* Connectez-vous au **panneau d'administration de Plesk**.
* Sélectionnez **Tools and Settings**.
* Cliquez sur **DNS Template Settings** dans la section.
* Sélectionnez **Localnets** dans la section **DNS Recursion**.
* Cliquez sur le bouton **OK**.

## Désactiver la récursivité dans Windows Server 2003 et 2008
{:#disable-recursion-in-windows-server}

* Utilisez le **Gestionnaire DNS** à partir du menu **Démarrer** :
  * Cliquez sur le bouton **Démarrer**.
  * Sélectionnez **Outils d'administration**.
  * Sélectionnez **DNS**.
* Cliquez avec le bouton droit de la souris sur le **serveur DNS** souhaité dans l'**arborescence de la console**.
* Sélectionnez l'onglet **Propriétés**.
* Cliquez sur le bouton **Avancé** dans la section **Options du serveur**.
* Cochez la case **Disable Recursion**.
* Cliquez sur le bouton **OK**.

## Désactiver la récursivité dans Linux
{:#disable-recursion-in-linux}

 * Localisez le fichier de configuration BIND dans le système d'exploitation. Le fichier de configuration BIND se trouve généralement dans l'un des chemins suivants :
  * /etc/bind/named.conf
  * /etc/named.conf
* Ouvrez le fichier named.conf dans votre éditeur préféré.
* Ajoutez les détails suivants dans la section **Options** :<br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* Redémarrez l'unité.
