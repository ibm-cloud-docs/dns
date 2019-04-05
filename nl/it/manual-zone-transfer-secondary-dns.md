---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Manual Zone Transfer, DNS Zone transfers, Secondary DNS Zone

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Esecuzione di un trasferimento di zona manuale per una zona DNS secondaria
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

In generale, i trasferimenti di zona DNS vengono completati automaticamente, in base all'intervallo di trasferimento DNS secondario da te specificato. Puoi utilizzare un trasferimento di zona manuale per forzare il trasferimento di contenuto per cui altrimenti bisognerebbe attendere fino al successivo trasferimento automatico. Per completare un trasferimento manuale, [è necessario stabilire una zona DNS secondaria](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone). Attieniti alla procedura in quest'articolo per eseguire un trasferimento di zona manuale per un DNS secondario.

1. Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). Fai riferimento a [Using the DNS Zones Screen](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window} (Utilizzo della schermata DNS Zones (Zone DNS)).
2. Per avviare il trasferimento, seleziona **Force Transfer** (Forza trasferimento) dall'elenco a discesa **Actions** (Azioni).

## Cosa succede poi
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone-next}

Una volta avviato il trasferimento, lo stato cambia e diventa **Transferring now** (Trasferimento in corso). I trasferimenti manuali non possono essere annullati, una volta iniziati. Dopo che i dati sono stati trasferiti, i trasferimenti di dati ritorneranno all'intervallo di trasferimento precedentemente impostato per il DNS secondario. L'[intervallo di trasferimento può essere modificato](/docs/infrastructure/dns?topic=dns-edit-a-secondary-dns-zone) in qualsiasi momento per evitare l'esigenza di eseguire trasferimenti di zona manuali frequentemente.
