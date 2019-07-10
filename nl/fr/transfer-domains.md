---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-15"

keywords: Transfer Existing Domain, Transfer multiple domains 

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Transfert de domaines
{: #transfer-domains}

## Transférer des domaines existants vers IBM Cloud
{:#transfer-an-existing-domain-to-ibm-cloud}

Une fois qu'un domaine a été enregistré, il peut être transféré à tout moment. Le transfert d'un domaine d'un registre tiers vers {{site.data.keyword.cloud}} peut rationaliser le processus de gestion de domaine. Le transfert d'un domaine n'affecte pas le site Web, l'e-mail ou le DNS. Il modifie uniquement le registre qui gère les enregistrements de domaine. Effectuez les étapes de cet article pour transférer un domaine existant vers {{site.data.keyword.cloud_notm}}.

## Transférer un seul domaine
{: #transfer-single-domain}

* Accédez à l'écran **Enregistrement de Domaine** sur la [console {{site.data.keyword.cloud_notm}}![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). Reportez-vous à la section [Accéder à l'écran d'enregistrement du domaine](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen).
* Sélectionnez l'onglet **Transférer**.
* Entrez le nom de domaine existant dans le champ **Nom de domaine**.
* Sélectionnez le type de domaine dans la liste déroulante **Type de domaine**.
* Sélectionnez la durée pendant laquelle le domaine restera actif dans la liste déroulante **Temps d'enregistrement**.

  Le prix de chaque période figure en regard de la durée et sera facturé sur la carte de paiement ou déduit du crédit porté au compte lors du renouvellement du domaine.
  {:note}
  
* Sélectionnez le bouton **Continuer** pour transférer le domaine.

## Transférer plusieurs domaines 
{: #transfer-multiple-domains}

Les domaines peuvent être transférés à {{site.data.keyword.cloud_notm}} en masse à tout moment, plutôt qu'individuellement, si une carte de crédit est active ou un crédit est disponible sur le compte. Effectuez les étapes suivantes pour transférer plusieurs domaines pour {{site.data.keyword.cloud_notm}}.

* Accédez à l'écran **Enregistrement de Domaine** sur la [console {{site.data.keyword.cloud_notm}}![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/). Reportez-vous à la section [Accéder à l'écran d'enregistrement du domaine](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen).
* Sélectionnez l'onglet **Transférer**.
* Sélectionnez l'option **Transférer plusieurs domaines ?** dans l'onglet **Transférer**.
* Entrez le nom de domaine existant dans le champ **Nom de domaine**.
* Sélectionnez le type de domaine dans la liste déroulante **Type de domaine**.
* Sélectionnez la durée pendant laquelle le domaine restera actif dans la liste déroulante **Temps d'enregistrement**.

Le prix de chaque période figure en regard de la durée et sera facturé sur la carte de paiement ou déduit du crédit porté au compte lors du renouvellement du domaine.
{:note}

* Répétez ces étapes pour chaque domaine supplémentaire à transférer.

Sélectionnez l'option **Ajouter** pour renseigner des champs vides supplémentaires et disposer ainsi de davantage d'entrées de domaine. Sélectionnez l'icône **Supprimer** pour supprimer une entrée complète de l'écran.
{:note}

* Sélectionnez le bouton **Continuer** pour transférer les domaines.



## Etapes suivantes
{:#transfer-an-existing-domain-to-ibm-cloud-next}

Après avoir transféré un domaine, vous pouvez le gérer dans le [portail client![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/). Lorsque l'enregistrement du domaine approche de sa date d'expiration, vous pouvez le [renouveler](/docs/infrastructure/dns?topic=dns-renew-an-existing-domain) dans l'écran **Gestion de domaine**.
