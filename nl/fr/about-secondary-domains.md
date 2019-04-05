---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary Domains, secondary domain, IBM Cloud DNS servers transfer

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# A propos des domaines secondaires
{:#about-secondary-domains}

Un domaine secondaire est un domaine que les serveurs DNS de {{site.data.keyword.BluSoftlayer_notm}} transfèrent de votre serveur à nos serveurs DNS faisant autorité, à savoir `ns1.softlayer.com` et `ns2.softlayer.com`.  Vous pouvez configurer un domaine secondaire dans le portail en cliquant sur **<span style="text-decoration: underline">Système de noms de domaine</span>** dans le dossier **<span style="text-decoration: underline">Réseau public</span>** du portail, en cliquant sur le lien **<span style="text-decoration: underline">DNS secondaire</span>** et enfin en cliquant sur **<span style="text-decoration: underline">Ajouter un enregistrement DNS secondaire</span>**.

Pour configurer un domaine secondaire, vous devez disposer de trois informations : le domaine, l'*adresse IP du serveur DNS principal* à partir duquel vous effectuez le transfert, et la fréquence en minutes à laquelle vous souhaitez que le domaine soit transféré.<br/>
Une fois qu'un domaine secondaire est configuré, vous pouvez modifier l'adresse IP du serveur maître et l'intervalle de transfert.  Vous serez également en mesure d'afficher le domaine au cours du transfert, de demander un transfert manuel, de convertir votre domaine secondaire en domaine principal et d'afficher tous les messages d'erreur consignés pendant le processus de transfert.
