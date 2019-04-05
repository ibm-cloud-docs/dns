---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, IBM Cloud, Add Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Ajouter une zone DNS secondaire
{:#add-a-secondary-dns-zone}

{{site.data.keyword.BluSoftlayer_notm}} fournit un DNS secondaire à tous les clients afin de mettre en cache les zones du DNS principal en cas de perte de données. Le maintien d'une zone DNS secondaire n'est pas obligatoire, mais il est vivement recommandé aux utilisateurs possédant plusieurs domaines. Effectuez les étapes ci-dessous pour ajouter une zone DNS secondaire :

* Accédez à l'écran **Zones DNS secondaires** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS > Zones en amont** dans le menu de navigation Infrastructure classique.
* Sélectionnez l'onglet **Ajouter zone**.
* Entrez le **domaine de la zone** dans le champ **Zone**.
* Entrez l'**adresse IP du serveur de noms principal** dans le champ **Serveur de noms maître**.
* Entrez la **durée de transfert (en minutes)** durant laquelle la zone DNS principale est transférée vers la zone DNS secondaire dans le champ d'**intervalle de transfert**.
* Sélectionnez le bouton **Ajouter** pour ajouter la zone ou sélectionnez **Annuler** pour annuler l'action.

## Etapes suivantes
{:#add-a-secondary-dns-zone-next}

Lorsqu'une zone DNS secondaire est créée, elle apparaît dans la liste des zones de l'écran Zones DNS secondaires. Le transfert des données de la zone principale vers la zone secondaire s'effectue à des intervalles que vous spécifiez lors de la création de la zone. A tout moment, vous pouvez [modifier](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record), [transférer manuellement](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) ou [convertir](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) la zone en zone principale. La zone DNS secondaire peut également être [supprimée](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone) à tout moment.
