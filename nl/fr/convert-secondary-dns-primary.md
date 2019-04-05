---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Convertir une zone DNS secondaire en une zone principale
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

A tout moment, une [zone DNS secondaire](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window} peut être convertie en zone principale. Lorsque vous convertissez une zone DNS secondaire en zone principale, les serveurs de noms {{site.data.keyword.BluSoftlayer_notm}} deviennent les serveurs de noms faisant autorité pour la zone convertie. Effectuez les étapes ci-dessous pour convertir une zone DNS secondaire en zone principale :

* Accédez à l'écran **Zones DNS secondaires** dans le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/) en sélectionnant **Infrastructure classique** dans le menu de navigation. 
* Sélectionnez **Réseau > DNS > Zones en amont** dans le menu de navigation Infrastructure classique.
* Sélectionnez **Convertir en zone principale** dans la liste déroulante **Actions** correspondant à la zone secondaire souhaitée.
* Sélectionnez le bouton **Oui** pour convertir la zone ou sélectionnez **Non** pour annuler l'action.

## Etapes suivantes
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

Après avoir converti la zone DNS secondaire en zone principale, vous pouvez l'afficher dans l'écran **Zones en aval**. Tous les enregistrements SOA et NS qui existaient auparavant pour la zone sont remplacés par les enregistrements SOA et NS {{site.data.keyword.BluSoftlayer_notm}} qui ne peuvent pas être modifiés. Vous pouvez toujours [modifier les enregistrements de zone restants](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record).
