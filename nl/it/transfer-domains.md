---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-15"

keywords: Transfer Existing Domain, Transfer multiple domains 

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Trasferimento di domini
{: #transfer-domains}

## Trasferisci i domini esistenti a IBM Cloud
{:#transfer-an-existing-domain-to-ibm-cloud}

Dopo essere stato registrato, un dominio può essere trasferito in qualsiasi momento. Il trasferimento di un dominio da un registrar di terze parti a {{site.data.keyword.cloud}} può semplificare il processo di gestione dei domini. Il trasferimento di un dominio non influenza il sito web, l'email o DNS. Modifica solo il registrar che gestisce i record di dominio. Attieniti alla procedura in questo articolo per trasferire un dominio esistente a {{site.data.keyword.cloud_notm}}.

## Trasferimento di un singolo dominio
{: #transfer-single-domain}

* Vai alla schermata **Domain Registration** (Registrazione dominio) della console di [{{site.data.keyword.cloud_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). Fai riferimento a [Access the Domain Registration Screen](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen) (Utilizzo della schermata DNS Zones (Zone DNS)).
* Scegli la scheda **Transfer** (Trasferisci).
* Immetti il nome dominio esistente nel campo **Domain Name** (Nome dominio).
* Seleziona il tipo di dominio dall'elenco a discesa **Domain Type** (Tipo di dominio).
* Seleziona la quantità di tempo per cui il dominio rimarrà attivo dall'elenco a discesa **Registration Time** (Tempo di registrazione).

  Il prezzo per ciascun periodo di tempo viene visualizzato accanto alla quantità di tempo e verrà addebitato sulla carta di credito o detratto dal credito nell'account quando viene rinnovato il dominio.
  {:note}
  
* Seleziona il pulsante **Continue** (Continua) per trasferire il dominio.

## Trasferimento di più domini
{: #transfer-multiple-domains}

I domini possono essere trasferiti a {{site.data.keyword.cloud_notm}} in blocco in qualsiasi momento, invece che singolarmente, se c'è una carta di credito attiva oppure del credito disponibile nell'account. Attieniti alla seguente procedura per trasferire più domini per {{site.data.keyword.cloud_notm}}.

* Vai alla schermata **Domain Registration** (Registrazione dominio) della console di [{{site.data.keyword.cloud_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). Fai riferimento a [Access the Domain Registration Screen](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen) (Utilizzo della schermata DNS Zones (Zone DNS)).
* Scegli la scheda **Transfer** (Trasferisci).
* Seleziona l'opzione **Transfer Multiple Domains?** (Trasferire più domini?) nella scheda **Transfer** (Trasferisci).
* Immetti il nome dominio esistente nel campo **Domain Name** (Nome dominio).
* Seleziona il tipo di dominio dall'elenco a discesa **Domain Type** (Tipo di dominio).
* Seleziona la quantità di tempo per cui il dominio trasferito rimarrà attivo dall'elenco a discesa **Registration Time** (Tempo di registrazione).

Il prezzo per ciascun periodo di tempo viene visualizzato accanto alla quantità di tempo e verrà addebitato sulla carta di credito o detratto dal credito nell'account quando viene rinnovato il dominio.
{:note}

* Ripeti per ogni dominio aggiuntivo da trasferire.

Seleziona l'opzione **Add Another** (Aggiungi un altro) per compilare ulteriori campi vuoti per altre voci di dominio. Seleziona l'icona **Delete** (Elimina) per eliminare un'intera voce dallo schermo.
{:note}

* Seleziona il pulsante **Continue** (Continua) per trasferire i domini.



## Cosa succede poi
{:#transfer-an-existing-domain-to-ibm-cloud-next}

Dopo aver trasferito un dominio, puoi gestirlo nel [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Quando la data di scadenza della registrazione del dominio è prossima, puoi [rinnovarla](/docs/infrastructure/dns?topic=dns-renew-an-existing-domain) dalla schermata **Domain Management** (Gestione dominio).
