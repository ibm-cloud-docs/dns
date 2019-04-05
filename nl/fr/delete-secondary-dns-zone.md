---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Supprimer une zone DNS secondaire
{:#delete-a-secondary-dns-zone}

Une fois qu'une zone DNS secondaire a été créée, elle peut être supprimée à tout moment. Sachez que si une zone DNS secondaire est supprimée, elle ne peut pas être récupérée. Effectuez les étapes ci-dessous pour supprimer un enregistrement DNS secondaire.

 * Accédez à l'écran **Zones DNS secondaires** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS > Zones en amont** dans le menu de navigation Infrastructure classique.
* Sélectionnez **Supprimer** dans la liste déroulante **Actions** pour la zone à supprimer. Une fenêtre contextuelle de confirmation apparaît.
  Si plusieurs zones secondaires existent, la vue peut être filtrée pour localiser la zone à supprimer.
  {:note}
* Sélectionnez le bouton **Oui** pour confirmer la suppression ou sélectionnez le bouton **Non** pour annuler l'action.

## Etapes suivantes
{:#delete-a-secondary-dns-zone-next}

Après la suppression d'une zone DNS secondaire, les transferts automatiques de la zone principale cessent et la zone secondaire n'existe plus. Si une zone DNS secondaire est requise à tout moment pour la zone principale, vous pouvez [créer une nouvelle DNS secondaire](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone).
