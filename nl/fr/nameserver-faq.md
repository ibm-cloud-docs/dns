---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: IBM Cloud name server addresses, Authoritative Name Servers, domain names

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# FAQ sur les serveurs de noms
{:#nameserver-faqs}

## Quelles sont les adresses des serveurs de noms IBM Cloud ?
{:#what-are-the-ibm-cloud-name-server-addresses}

Il existe deux adresses pour les serveurs de noms faisant autorité et deux adresses pour les serveurs de noms de résolution.

**Serveurs de noms faisant autorité**

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

**Serveurs de noms de résolution**

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12


## Quelle est la différence entre les serveurs de noms publics et privés de SoftLayer ?
{:#what-is-the-difference-public-private-nameserver}

Les serveurs de noms publics agissent en tant que serveurs de noms faisant autorité pour les noms de domaine résidant sur les serveurs DNS et gérés via le portail client. Ces serveurs "répondent aux" et "résolvent" les noms de domaine en votre adresse IP pour les utilisateurs généraux d'Internet.

Les serveurs de noms de résolution sont situés sur le réseau privé et agissent en tant que programmes de résolution DNS pour votre serveur. Les programmes de résolution privés interrogent les serveurs de noms racine d'Internet pour les recherches de domaine. Par exemple, l'envoi de courrier à partir de votre serveur nécessite une recherche NSlookup du nom de domaine de destination. Les serveurs DNS privés résolvent ces informations sur le réseau privé pour réduire l'utilisation de la bande passante, réduire la charge sur les serveurs faisant autorité et offrir une résolution rapide. Les programmes de résolution de réseaux privés constituent un service pratique pour nos clients.

## Quelles sont mes options de serveur de noms ?
{:#what-are-my-name-server-options}

Avec un serveur Bare Metal, il existe quatre options type pour les serveurs de noms :

1. Utilisez les serveurs de noms de registre de noms de domaine pour gérer vos noms de domaine.
2. Utilisez les serveurs de noms IBM Cloud pour gérer vos noms de domaine.
3. Utilisez un service DNS tiers pour gérer vos noms de domaine.
4. Exécutez vos propres serveurs de noms sur votre serveur pour gérer vos noms de domaine.

Pour les options 1, 2 & 3, utilisez les serveurs de noms du tiers (par exemple, `ns1.softlayer.com` et `ns2.softlayer.com`). Pour l'option numéro 4, utilisez votre domaine en tant que serveur de noms (`ns1.yourdomain.com` & `ns2.yourdomain.com`). L'option numéro 4 impose l'exécution des services DNS sur le serveur, et vous devez également enregistrer votre domaine en tant que serveur de noms auprès de votre registre. Cet enregistrement est généralement gratuit, mais il nécessite une étape supplémentaire, outre le processus d'enregistrement du nom de domaine de base.

IBM Cloud propose des services DNS gratuits entièrement gérés via le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). Nous vous recommandons vivement d'autoriser IBM Cloud à gérer votre DNS et à agir en tant que serveurs de noms, car nous disposons de systèmes redondants, faciles à gérer et capables de résoudre rapidement les problèmes liés au DNS.


## Comment puis-je utiliser mes propres serveurs de noms ?
{:#how-can-i-run-my-own-nameservers}

Le moyen le plus simple d'exécuter et de gérer vos propres serveurs de noms consiste à utiliser un outil de panneau de contrôle tel que **Plesk** ou **cPanel**. Ces deux produits comportent des serveurs de noms de domaine intégrés qui vous permettent d'ajouter, de modifier ou de supprimer des noms de domaine.

Pour commencer, enregistrez votre nom de domaine en tant que serveur de noms auprès de votre registre de noms de domaine et attribuez deux adresses IP à partir des plages IP de votre ou vos serveurs.
