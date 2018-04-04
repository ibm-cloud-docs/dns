---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Mettre à jour un enregistrement DNS en amont

Un DNS en amont permet aux utilisateurs d'identifier le domaine associé à une adresse IP. Les clients peuvent mettre à jour leurs enregistrements DNS en amont à tout moment pour modifier le PTR et la durée de vie (TTL). Dans le [portail client version **Gérer** ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/), vous pouvez mettre à jour des enregistrements PTR en masse à l'aide de l'outil de **recherche et remplacement**. Cet outil vous permet d'entrer tout ou partie d'un PTR dans le champ de recherche et de remplacer chaque occurrence dans les PTR correspondants par les informations souhaitées.  

Veuillez noter que cet outil ne fonctionne que lorsque les PTR existants sont associés au serveur ou au VLAN. S'il n'existe aucun PTR, aucun détail n'est répertorié et les tentatives de mise à jour entraînent une erreur.  

Pour ajouter un enregistrement PTR de DNS en amont, reportez-vous à [Ajouter et modifier un enregistrement PTR (Pointeur)](add-and-edit-ptr-pointer-record.html). Effectuez ces étapes pour mettre à jour un enregistrement DNS en amont : 

 * Accédez au [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/) à l'aide de vos identifiants uniques.
 * Sélectionnez **DNS** dans le menu déroulant **Réseau**.
 * Sélectionnez l'option de menu **DNS en amont**. 
 * Déterminez si la mise à jour doit être effectuée sur toutes les adresses IP correspondantes au réseau VLAN ou si des modifications doivent être apportées à une adresse IP individuelle. <br><br><table border="1"><tbody><tr><th>Si la mise à jour doit être effectuée sur...</th><th>Alors...</th></tr><tr><td>Une adresse IP individuelle</td><td><ul><li>Sélectionnez le <b>menu déroulant</b> pour afficher les adresses IP </li><li>Cliquez sur l'<strong>adresse IP</strong> souhaitée pour afficher les informations associées au serveur sur le DNS en amont. </li></ul></td></tr><tr><td>Toutes les adresses IP correspondantes sur un réseau local virtuel </td><td><ul><li>Sélectionnez l'option <strong>Afficher IP</strong> après avoir sélectionné une adresse IP comme indiqué ci-dessus. </li><li>Sélectionnez l'option <strong>Editer le RDNS pour toutes les adresses IP de ce sous-réseau</strong>.</li></ul></td></tr></tbody></table><br/>
 * Pour les adresses IP individuelles, ajoutez simplement le **nom d'hôte** et la **Durée de vie en amont**, puis sélectionnez **Sauvegarder**. Pour l'intégralité du **Sous-réseau**, mettez en surbrillance l'espace libre sous la colonne **DNS en amont** et ajoutez le **nom d'hôte**, puis sélectionnez le bouton **Mettre à jour**. Cette tâche devra être effectuée pour chaque adresse IP du sous-réseau. 
