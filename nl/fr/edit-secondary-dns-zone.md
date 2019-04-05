---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Master Nameserver

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Modifier une zone DNS secondaire
{:#edit-a-secondary-dns-zone}

Les zones DNS secondaires peuvent être modifiées à tout moment pour mettre à jour le serveur de noms maître ou l'intervalle de transfert. Effectuez les étapes ci-dessous pour modifier une zone DNS secondaire.

* Accédez à l'écran **Zones DNS secondaires** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS > Zones en amont** dans le menu de navigation Infrastructure classique.
* Cliquez n'importe où sur la **ligne contenant la zone DNS secondaire** pour ouvrir la zone pour les modifications.
  Si plusieurs zones secondaires existent, la vue peut être filtrée pour localiser la zone à modifier.
  {:note}  
* Mettez à jour les champs **Serveur de noms maître** et **Intervalle de transfert** si nécessaire.
* Sélectionnez le bouton **Mettre à jour** pour mettre à jour la zone DNS secondaire ou sélectionnez **Annuler** pour annuler l'action.

## Etapes suivantes
{:#edit-a-secondary-dns-zone-next}

Après modification de la zone DNS secondaire, les valeurs **Serveur de noms maître** et **Intervalle de transfert** reflètent la mise à jour et la zone secondaire commence à recevoir des transferts basés sur les nouvelles informations. A tout moment, vous pouvez modifier la zone à nouveau en répétant les étapes ci-dessus.
