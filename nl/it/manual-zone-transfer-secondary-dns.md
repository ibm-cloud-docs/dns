---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Esecuzione di un trasferimento di zona manuale per una zona DNS secondaria

In generale, i trasferimenti di zona DNS vengono completati automaticamente, in base all'intervallo di trasferimento DNS secondario da te specificato. Puoi utilizzare un trasferimento di zona manuale per forzare il trasferimento di contenuto per cui altrimenti bisognerebbe attendere fino al successivo trasferimento automatico. Per completare un trasferimento manuale, [è necessario stabilire una zona DNS secondaria](add-secondary-dns-zone.html). Attieniti alla procedura in quest'articolo per eseguire un trasferimento di zona manuale per un DNS secondario.

1. Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Fai riferimento a [Using the DNS Zones Screen](delete-secondary-dns-record.html){:new_window} (Utilizzo della schermata DNS Zones (Zone DNS)).
2. Per avviare il trasferimento, seleziona **Force Transfer** (Forza trasferimento) dall'elenco a discesa **Actions** (Azioni).

## Cosa succede poi

Una volta avviato il trasferimento, lo stato cambia e diventa **Transferring now** (Trasferimento in corso). I trasferimenti manuali non possono essere annullati, una volta iniziati. Dopo che i dati sono stati trasferiti, i trasferimenti di dati ritorneranno all'intervallo di trasferimento precedentemente impostato per il DNS secondario. L'[intervallo di trasferimento può essere modificato](edit-secondary-dns-zone.html) in qualsiasi momento per evitare l'esigenza di eseguire trasferimenti di zona manuali frequentemente.
