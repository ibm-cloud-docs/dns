---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Conversione di una zona DNS secondaria in una zona primaria

In qualsiasi momento, è possibile convertire una [zona DNS secondaria](add-secondary-dns-zone.html){:new_window} nella tua nuova zona primaria. Quando converti una zona DNS secondaria in primaria, i server dei nomi {{site.data.keyword.BluSoftlayer_notm}} diventano server dei nomi autorevoli per la zona convertita. Attieniti alla procedura di seguito per convertire una zona DNS secondaria in primaria:

* Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Fai riferimento a [Using the DNS Zones Screen](use-dns-zones-screen.html){:new_window} (Utilizzo della schermata DNS Zones (Zone DNS)).
* Seleziona **Convert to Primary** (Converti in primaria) dall'elenco a discesa **Actions** (Azioni) per la zona secondaria desiderata.
* Seleziona il pulsante **Yes** (Sì) per convertire la zona oppure seleziona **No** per annullare l'azione.

## Cosa succede poi

Dopo che hai convertito la zona DNS secondaria in primaria, puoi visualizzarla nella schermata **Forward Zones** (Zone di inoltro). Tutti i record SOA e NS che esistevano in precedenza per la zona verranno sostituiti da record SOA ed NS {{site.data.keyword.BluSoftlayer_notm}}, che non possono essere modificati. Puoi però ancora [modificare i restanti record di zona](edit-dns-zone-record.html).
