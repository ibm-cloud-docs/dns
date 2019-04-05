---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: domain names, Resource Records, host name

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Présentation du DNS - Enregistrements de ressources
{:#dns-0verview-resource-records}

## Section d'enregistrement `A`
{:#the-a-record-section}

La plupart des enregistrements sont des enregistrements **A**. Ils offrent la polyvalence maximale en vous permettant de diriger vos noms de domaine où vous le souhaitez. Chaque enregistrement comprend un nom d'hôte et une adresse IP.

**Champ Hôte :** nom d'hôte de cet enregistrement A particulier. Le nom d'hôte doit être la partie qui précède le domaine _.domain.com_ dans votre nom FQDN (nom de domaine complet). Par exemple, sur `www.domain.com`, "www" désigne l'hôte (sans guillemets). La recherche ajoute automatiquement ".domain.com" à la requête. Un "enregistrement A" vide (_domain.com_ plutôt que _host.domain.com_) est créé en plaçant le signe '@' dans le champ du nom d'hôte.

Les enregistrements "A" communs incluent : `www.domain.com`, `ftp.domain.com`, `mail.domain.com`, `webmail.domain.com`, `mysql.domain.com`

**Champ Pointe vers :** ce champ vous permet d'indiquer l'adresse IP vers laquelle le nom d'hôte doit pointer.

## Section `CNAME`
{:#the-cname-section}

Les enregistrements CNAME pointent vers des noms de domaine au lieu d'adresses IP. L'avantage d'utiliser un enregistrement CNAME est que vous pouvez faire pointer un hôte vers un nom de domaine particulier, puis modifier uniquement les enregistrements A du nom de domaine cible pour que la modification ait lieu sur les deux domaines. Cette méthode est couramment utilisée par les personnes possédant, pour le même domaine, plusieurs domaines de niveau supérieur (TLD) en différentes versions (.com, .net, .org, etc.).

Par exemple, vous possédez `_domain.com_` et `_domain.net_`, et vous voulez que les enregistrements pointent vers la même adresse IP. Vous pouvez créer des enregistrements CNAME pour l'hôte _www_ de `_domain.net_` qui pointent vers `www.domain.com`. Ensuite, pour modifier l'hôte _www_ de `_domain.net_`, ils vous suffit de modifier l'enregistrement A de `www.domain.com` afin qu'il pointe vers sa nouvelle adresse IP, et `www.domain.net` sera également modifié automatiquement.

Une erreur courante de l'utilisation de cette méthode est que vous pouvez modifier accidentellement les enregistrements de plusieurs domaines alors vous souhaitiez n'en modifier qu'un seul. Autrement dit, vous _devez_ noter quels domaines pointent les uns vers les autres.

**Champ Hôte :** nom d'hôte de cet enregistrement CNAME particulier. Le nom d'hôte doit être la partie qui précède le domaine _.domain.com_ dans votre nom FQDN (nom de domaine complet). Par exemple, sur `www.domain.com`, “www” désigne l'hôte (sans guillemets). La recherche ajoute automatiquement “`.domain.com`” à la requête. Un "enregistrement A" (`_domain.com_` plutôt que `_host.domain.com_`) est créé en plaçant le signe `@` dans le champ du nom d'hôte.

**Champ Pointe vers :** nom vers lequel pointe l'enregistrement. _Ce champ doit être un nom de domaine et non une adresse IP._ Le nom de domaine doit également se terminer par un point. Si tel n'est pas le cas, lorsqu'il est interrogé, l'enregistrement de domaine continue jusqu'à ce qu'il trouve le point suivant dans le fichier de zone.

## Section `MX`
{:#the-mx-section}

La section MX est la zone qui gère la direction du courrier.

**Champ Priorité :** cette section vous permet de sélectionner votre préférence pour un enregistrement MX individuel. Les enregistrements sont traités dans l'ordre, en commençant par la priorité la plus faible et en procédant vers des priorités plus élevées. Par conséquent, si vous disposez de deux serveurs de messagerie ou d'un serveur de messagerie et d'un spouleur de messagerie, définissez la priorité inférieure sur votre serveur de messagerie principal et une priorité plus élevée sur votre serveur de messagerie de secours ou sur le spouleur de messagerie.

**Champ Hôte :** vous pouvez spécifier un nom d'hôte de messagerie ici, mais dans la plupart des cas, cela n'est pas nécessaire. Il est recommandé de créer un hôte vide (utilisez le signe `@` pour le nom d'hôte) et de le faire pointer sur le serveur de messagerie.

**Champ Va :** adresse du serveur de messagerie. L'usage courant consiste à utiliser le nom d'hôte de messagerie créé à la section d'enregistrement A pour pointer vers votre messagerie.

Il est vivement conseillé de faire pointer les enregistrements MX vers un nom de domaine, et ce nom de domaine (comme un enregistrement CNAME) doit se terminer par un point.

## Section `TXT`
{:#the-txt-section}

Un enregistrement TXT est généralement un enregistrement que vous pouvez interroger et qui renvoie des informations sur un domaine. Ces enregistrements peuvent être utilisés pour les indicateurs SPF, pour créer des connexions de port et de protocole ou simplement pour renvoyer des informations sur un domaine. Ils sont le plus souvent utilisés avec le protocole SPF.

**Nom :** hôte par lequel l'enregistrement TXT peut être interrogé.

**Valeur :** renvoyée par l'enregistrement TXT, placée entre guillemets.
