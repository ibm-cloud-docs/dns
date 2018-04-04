---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Supprimer une zone DNS secondaire 

Une fois qu'une zone DNS secondaire a été créée, elle peut être supprimée à tout moment. Sachez que si une zone DNS secondaire est supprimée, elle ne peut pas être récupérée. Effectuez les étapes ci-dessous pour supprimer un enregistrement DNS secondaire. 

 * Accédez à l'écran de **Zones DNS secondaire** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/). Reportez-vous à la section [Utilisation de l'écran de zones DNS](use-dns-zones-screen.html){:new_window}.
* Sélectionnez **Supprimer** dans la liste déroulante **Actions** pour la zone à supprimer. Une fenêtre contextuelle de confirmation apparaît. **Remarque :** si plusieurs zones secondaires existent, la vue peut être filtrée pour localiser la zone à supprimer.
* Sélectionnez le bouton **Oui** pour confirmer la suppression ou sélectionnez le bouton **Non** pour annuler l'action. 

## Etapes suivantes

Après la suppression d'une zone DNS secondaire, les transferts automatiques de la zone principale cessent et la zone secondaire n'existe plus. Si une zone DNS secondaire est requise à tout moment pour la zone principale, vous pouvez [créer une nouvelle DNS secondaire](add-secondary-dns-zone.html).
