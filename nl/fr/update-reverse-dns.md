---
copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-02-26"

keywords: Reverse DNS Record, Reverse DNS, IP address, Individual IP Select

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Mettre à jour un enregistrement DNS en amont
{:#update-reverse-dns-record}

Un DNS en amont permet aux utilisateurs d'identifier le domaine associé à une adresse IP. Les clients peuvent mettre à jour leurs enregistrements DNS en amont à tout moment pour modifier le PTR et la durée de vie (TTL). Dans la version **Gérer** de la [Console IBM Cloud ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/), vous pouvez mettre à jour les enregistrements PTR en bloc, à l'aide de l'outil **Search and Replace**. Cet outil vous permet d'entrer tout ou partie d'un PTR dans le champ de recherche et de remplacer chaque occurrence dans les PTR correspondants par les informations souhaitées. 

Veuillez noter que cet outil ne fonctionne que lorsque les PTR existants sont associés au serveur ou au VLAN. S'il n'existe aucun PTR, aucun détail n'est répertorié et les tentatives de mise à jour entraînent une erreur. 

Pour ajouter un enregistrement PTR de DNS en amont, reportez-vous à [Ajouter et modifier un enregistrement PTR (Pointeur)](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record). Effectuez ces étapes pour mettre à jour un enregistrement DNS en amont :

 * Accédez à la [Console IBM Cloud ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) à l'aide de vos identifiants uniques.
 * Sélectionnez **Infrastructure classique** dans le menu de navigation.
 * Sélectionnez **Réseau > DNS > DNS en amont** dans le menu de navigation Infrastructure classique.
 * Entrez l'adresse IP, ou sélectionnez-la dans le menu déroulant, puis cliquez sur **Afficher IP**.
 * Modifiez les options répertoriées et cliquez sur **Sauvegarder**. Vous pouvez également choisir **Éditer le RDNS pour toutes les adresses IP de ce sous-réseau** afin d'apporter les modifications à l'ensemble du sous-réseau. 
 

