---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Modifica di una zona DNS secondaria

Le zone DNS secondarie possono essere modificate in qualsiasi momento per aggiornare il server dei nomi master o l'intervallo di trasferimento. Attieniti alla seguente procedura per modificare una zona DNS secondaria.

* Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Fai riferimento a [Using the DNS Zones Screen](delete-secondary-dns-record.html){:new_window} (Utilizzo della schermata DNS Zones (Zone DNS)).
* Fai clic in qualsiasi punto della **riga che contiene la zona DNS secondaria** per aprire la zona per le modifiche.
  * **Nota:** se esistono più zone secondarie, la vista può essere filtrata per individuare la zona a cui si devono apportare le modifiche.
* Aggiorna i campi **Master Nameserver** (Server dei nomi master) e **Transfer Interval** (Intervallo di trasferimento) come necessario.
* Seleziona il pulsante **Update** (Aggiorna) per aggiornare la zona DNS secondaria oppure seleziona **Cancel** (Annulla) per annullare l'azione.

## Cosa succede poi

Dopo aver modificato la zona DNS secondaria, i valori **Master Nameserver** (Server dei nomi master) e **Transfer Interval** (Intervallo di trasferimento) rifletteranno l'aggiornamento e la zona secondaria inizierà a ricevere i trasferimenti sulla base delle nuove informazioni. Puoi modificare di nuovo la zona in qualsiasi momento ripetendo la procedura sopra indicata.
