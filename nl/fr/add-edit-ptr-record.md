---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Record PTR, IP addresses, Reverse DNS feature

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Ajouter ou modifier un enregistrement PTR (pointeur)
{:#add-or-edit-a-ptr-pointer-record}

Un enregistrement PTR, ou pointeur, enregistre les adresses IP dans des noms d'hôtes. Les utilisateurs peuvent ajouter des enregistrements PTR à associer à une adresse IP à l'aide de la fonctionnalité de DNS en amont sur le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/){:new_window}. En outre, les enregistrements PTR peuvent être modifiés de la même manière qu'ils sont ajoutés. Effectuez les étapes ci-dessous pour ajouter ou modifier un enregistrement PTR pour une unité :

* Récupérez l'**Adresse IP publique** de l'unité qui reçoit l'enregistrement PTR dans la **Liste des unités**.
* Affichez l'écran **Enregistrements de DNS en amont**** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS > DNS en amont** dans le menu de navigation Infrastructure classique.
* Entrez l'**Adresse IP publique** récupérée dans la liste des unités dans le champ **Afficher IP**.
* Cliquez n'importe où sur la ligne contenant les détails de l'**Enregistrement en amont** pour ouvrir la ligne pour modification.
* Complétez ou mettez à jour les champs de l'enregistrement en fonction du tableau ci-dessous :<br/><br/><table border="1"><tbody><tr><th>Champ</th><th>Entrée</th></tr><tr><td>DNS en amont</td><td>Nom d'hôte en lequel l'adresse IP est résolue.</td></tr><tr><td>Durée de Vie en Amont</td><td>Durée de vie (TTL) du nouvel enregistrement</td></tr><tr><td>Remarques</td><td>Toutes les remarques applicables au dossier</td></tr></tbody></table><br/>
* Cliquez sur le bouton **Mettre à jour** pour mettre à jour l'enregistrement. Cliquez sur **Annuler** pour annuler l'action.

## Etapes suivantes
{:#add-or-edit-a-ptr-pointer-record-next}

Après l'ajout d'un enregistrement PTR, l'adresse IP publique associée à cet enregistrement est résolue en nom d'hôte spécifié dans l'enregistrement. L'enregistrement peut être modifié à tout moment. Pour supprimer les détails de l'enregistrement PTR, supprimez toutes les informations des champs à l'aide du processus d'**édition**.
