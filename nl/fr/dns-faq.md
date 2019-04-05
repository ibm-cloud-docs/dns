---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-13"

keywords: DNS servers, fast domain name resolution, DNS FAQ

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}


# FAQ DNS
{:#dns-faq}

## Quels sont les serveurs DNS ?
{:#what-are-dns-servers}
{: faq}

161.26.0.10 et 161.26.0.11

## Quels sont les programmes de résolution DNS locaux ?
{:#what-are-local-dns-resolvers}
{: faq}

Les serveurs de noms locaux de programme de résolution sur notre réseau privé sont :

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Ces serveurs de noms fournissent une résolution de nom de domaine rapide qui n'utilise pas votre allocation de bande passante publique. Pour les utiliser, veuillez appliquer la procédure correcte pour ajouter des serveurs de noms de programme de résolution à votre système d'exploitation.

## Quelles sont les adresses de serveur de noms {{site.data.keyword.BluSoftlayer_notm}} ?
{:#what-are-name-server-addresses}
{: faq}

Il existe deux adresses pour les serveurs de noms faisant autorité et deux adresses pour les serveurs de noms de résolution.

### Serveurs de noms faisant autorité
{:#authoratative-name-servers}

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### Serveurs de noms de résolution
{:#resolving-name-servers}

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Ces serveurs de noms de résolution locaux se trouvent sur notre réseau privé, donc ils n'utilisent pas votre allocation de bande passante publique. 

## Quels serveurs DNS IBM Cloud répondent pour mes domaines secondaires ?
{:#what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}

Les serveurs DNS faisant autorité, activés IPv de {{site.data.keyword.BluSoftlayer_notm}} Anycast répondent pour vos domaines secondaires. Ces serveurs se trouvent aux adresses suivantes :

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## Quelles adresses IP sont utilisées pour mes transferts de zone de domaine secondaire ?
{:#which-ipaddresses-secondary-domain-zone-transfers}
{: faq}

Les transferts pour vos domaines secondaires proviennent de l'une des quatre adresses IP suivantes :

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## Quelle est la différence entre les serveurs de noms publics et privés ?
{:#public-v-private-nameservers}
{: faq}

Nos serveurs de noms publics agissent en tant que serveurs de noms faisant autorité pour les noms de domaine résidant dans nos serveurs DNS et gérés via le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). Ces serveurs "répondent aux" et "résolvent" les noms de domaine en votre adresse IP pour les utilisateurs généraux d'Internet.

Les serveurs de noms de résolution sont situés sur le réseau privé et agissent en tant que programmes de résolution DNS pour votre serveur. Les programmes de résolution privés interrogent les serveurs de noms racine d'Internet pour les recherches de domaine. Par exemple, l'envoi de courrier à partir de votre serveur nécessite une recherche NSlookup du nom de domaine de destination. Les serveurs DNS privés résolvent ces informations sur le réseau privé pour réduire l'utilisation de la bande passante, réduire la charge sur les serveurs faisant autorité et offrir une résolution rapide. Les programmes de résolution de réseaux privés constituent un service pratique pour nos clients.

## Quelles sont mes options de serveur de noms ?
{:#what-are-my-name-server-options-faq}
{: faq}

Avec un serveur Bare Metal, il existe quatre options type pour les serveurs de noms :

* Utilisez les serveurs de noms de votre registre de noms de domaine pour gérer vos noms de domaine.
* Utilisez les serveurs de noms {{site.data.keyword.BluSoftlayer_notm}} pour gérer vos noms de domaine.
* Utilisez un service DNS tiers pour gérer vos noms de domaine.
* Exécutez vos propres serveurs de noms sur votre serveur pour gérer vos noms de domaine.

Pour les trois premières options, utilisez les serveurs de noms du tiers (par exemple, `ns1.softlayer.com` et `ns2.softlayer.com`). La dernière option utilise votre domaine comme serveur de noms (par exemple,`ns1.yourdomain.com` & `ns2.yourdomain.com`), et vous oblige à exécuter les services DNS sur votre serveur. Vous devez également enregistrer votre domaine en tant que serveur de noms dans votre registre. L'enregistrement du serveur de noms est généralement gratuit, mais il nécessite une étape supplémentaire outre le processus d'enregistrement du nom de domaine de base.

Nos clients disposent de services DNS gratuits entièrement gérés via le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). Nous vous recommandons vivement d'autoriser {{site.data.keyword.BluSoftlayer_notm}} à gérer votre DNS et vos serveurs de noms, car nous disposons de systèmes redondants, faciles à gérer et capables de résoudre rapidement les problèmes liés au DNS.

## Comment puis-je configurer mon DNS en amont ?
{:#how-do-i-setup-reverse-dns}
{: faq}

La configuration DNS en amont s'effectue à l'aide de notre [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). Pour obtenir des instructions sur la configuration de votre DNS en amont, reportez-vous à la section [Mettre à jour un enregistrement DNS en amont](/docs/infrastructure/dns?topic=dns-update-a-reverse-dns-record).


## Combien de temps faut-il pour que les changements DNS se propagent ?
{:#how-long-for-dns-changes-propagate}
{: faq}

La durée de propagation des changements DNS dépend du paramètre de durée de vie (TTL) de l'enregistrement DNS.

La durée de vie par défaut est un jour, ce qui signifie que les changements apportés à un nom de domaine se propagent en un jour sur Internet. La durée de vie peut être réduite si vous prévoyez d'apporter des changements fréquemment. Cependant, plus la durée de vie est basse, plus la charge augmente sur le serveur de noms. Des charges plus élevées peuvent augmenter le temps de réponse pour les utilisateurs finaux, ce qui pourrait avoir une incidence sur leur satisfaction globale.

Plus le paramètre de durée de vie est élevé, plus les performances DNS seront élevées en raison de la mise en cache locale des FAI. Plus le paramètre de durée de vie est bas, plus les performances du DNS seront faibles en raison de l'augmentation des résolutions de noms.

Pour vérifier la durée de vie, vérifiez l'enregistrement Start of Authority (SOA) du domaine. Un excellent outil pour l'examen des informations de domaine est offert par [CentralOps.net ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://centralops.net/co/)

La durée de vie est exprimée en secondes. Divisez par 60 pour convertir la durée de vie en minutes, ou par 3600 pour la convertir en heures.


## Après transfert d'un domaine, combien de temps faut-il pour que le domaine et les modifications apparaissent ?
{:#how-long-transfer-change-visiblity}
{: faq}

Votre domaine et/ou vos modifications sont visibles sur les serveurs DNS IBM Cloud immédiatement après la fin du transfert. En raison de la nature de la propagation sur DNS, il se produit un délai avant que les modifications soient visibles sur d'autres serveurs DNS.

## Puis-je effectuer les demandes AXFR sur le réseau privé ?
{:#axfr-request-private-network}
{: faq}

Actuellement, {{site.data.keyword.BluSoftlayer_notm}} ne prend pas en charge la requête AXFR sur le réseau privé. Toutes les demandes AXFR doivent être effectuées sur le réseau public.
