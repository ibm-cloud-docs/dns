---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Initiation à DNS

Le DNS (Domain Name System) d'Internet est une méthode de traduction des adresses IP que les serveurs et les routeurs reconnaissent en des noms donnés, conviviaux, appelés _noms de domaine_ (par exemple `ibm.com`). 

Bien que le concept de DNS soit simple, la gestion et le stockage des enregistrements pour vos différents domaines peuvent devenir assez fastidieux en l'absence de méthode pratique. 

Le DNS IBM Cloud permet à ses clients de centraliser l'affichage et la gestion de leurs domaines à l'aide de l'interface de gestion DNS de base. Il permet également aux utilisateurs de gérer le DNS en amont et le DNS secondaire au même emplacement, gratuitement. 

IBM Cloud propose également une suite d'[outils réseau](https://console.bluemix.net/docs/infrastructure/network-tools/getting-started.html#getting-started-with-network-tools) supplémentaires. Pour obtenir des instructions spécifiques sur l'utilisation de l'interface DNS via le [portail client![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/), [veuillez consulter ce document](https://github.ibm.com/Bluemix-Docs/dns/blob/staging/using-the-dns-interface.html).

## Fonctionnement 
A la base, {{site.data.keyword.BluSoftlayer_notm}} DNS fonctionne de la même manière que n'importe quel outil de gestion DNS. Vous avez la possibilité d'interagir avec et de modifier des enregistrements DNS existants, d'ajouter de nouveaux enregistrements et de mettre à jour des informations sur le DNS en amont. Comparé à un autre service de gestion DNS ou une gestion par l'utilisateur lui-même, l'utilisation de {{site.data.keyword.BluSoftlayer_notm}} présente l'avantage de mettre à disposition un emplacement central et fiable pour le stockage de toutes vos données. 

En outre, {{site.data.keyword.BluSoftlayer_notm}} offre gratuitement des zones DNS secondaires à ses utilisateurs, ce qui leur permet de sauvegarder leurs enregistrements de DNS principal en cas de perte de données ou de panne sur le noeud. 

## Gestion du DNS
La plupart des utilisateurs gèrent leur DNS principal, en amont et secondaire à l'aide de notre [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/). A partir de ce portail, vous pouvez gérer tous vos éléments DNS. 

Vous avez également la possibilité d'utiliser l'API IBM Cloud SoftLayer (SLAPI) pour les interactions DNS. La fonctionnalité de l'API est presque identique à l'interface utilisateur du portail. Toutefois, si vous modifiez des enregistrements DNS en masse, le portail client fournit un maximum de 20 ensembles, tandis que l'API offre plus de flexibilité. Pour plus d'informations sur l'interaction avec DNS à l'aide de SLAPI, reportez-vous à la [documentation de cette API](dns-api.html).


