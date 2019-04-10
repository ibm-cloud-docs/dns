---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: IBM Cloud DNS, DNS

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Introduzione a DNS
{:#getting-started-with-dns}

Il DNS (Domain Name System) di Internet è un metodo di conversione degli indirizzi IP riconosciuti da server e router in specifici nomi descrittivi detti _nomi dominio_ (ad esempio, `ibm.com`).

Sebbene il concetto di DNS sia semplice, gestire e archiviare i record per i tuoi vari domini può diventare piuttosto tedioso, se non è disponibile un modo pratico per farlo.

DNS di IBM Cloud offre ai clienti un'ubicazione centrale da cui visualizzare e gestire i loro domini utilizzando la nostra interfaccia di gestione DNS di base. Offre anche agli utenti l'opzione di gestire DNS inverso e secondario nella stessa ubicazione, senza costi aggiuntivi.

IBM Cloud offre anche una suite di [strumenti di rete](/docs/infrastructure/network-tools?topic=network-tools-gettingstarted-with-network-tools#gettingstarted-with-network-tools) aggiuntivi. Per istruzioni specifiche sull'utilizzo della nostra interfaccia DNS tramite il [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/), consulta [Come utilizzare l'interfaccia DNS](/docs/infrastructure/dns?topic=dns-how-to-use-the-dns-interface).

## Come funziona
{:#how-dns-works}

Fondamentalmente, DNS di {{site.data.keyword.BluSoftlayer_notm}} funziona in modo analogo a qualsiasi strumento di gestione di DNS da te eventualmente utilizzato. Puoi interagire con i record DNS esistenti e modificarli, puoi aggiungerne di nuovi e puoi aggiornare le informazioni sul DNS inverso. Il principale vantaggio derivante dall'utilizzare {{site.data.keyword.BluSoftlayer_notm}} rispetto a un altro servizio di gestione dei DNS o anche dall'occuparti tu stesso della sua gestione consiste nell'avere un'ubicazione centrale e affidabile in cui sono archiviati tutti i tuoi dati.

Come servizio aggiuntivo, {{site.data.keyword.BluSoftlayer_notm}} offre zone DNS secondarie ai nostri clienti gratuitamente, consentendo agli utenti di eseguire un backup dei loro record DNS primari in caso di perdita di dati o di malfunzionamento di nodi.

## Come gestire i DNS
{:#how-to-manage-dns}

Gli utenti host gestiscono i loro DNS primario, inverso e secondario utilizzando il nostro [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). Il portale è la nostra interfaccia facilissima da usare (ti basta puntare il mouse e fare clic) per gestire tutto quanto concerne i DNS.

Puoi anche usare l'API di IBM Cloud SoftLayer (SLAPI) per le interazioni DNS. La funzionalità dell'API rispetto alla nostra IU del Portale è praticamente identica. Tuttavia, se stai modificando dei record DNS in blocco, il Portale del cliente consente di eseguire operazioni in blocco al massimo in gruppi da 20, mentre l'API offre maggiore flessibilità. Per ulteriori informazioni sull'interazione con DNS utilizzando la SLAPI, consulta [questa documentazione dell'API](/docs/infrastructure/dns?topic=dns-getting-started-with-the-dns-api).


