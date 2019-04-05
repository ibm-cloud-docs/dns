---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Master Nameserver

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Modifica di una zona DNS secondaria
{:#edit-a-secondary-dns-zone}

Le zone DNS secondarie possono essere modificate in qualsiasi momento per aggiornare il server dei nomi master o l'intervallo di trasferimento. Attieniti alla seguente procedura per modificare una zona DNS secondaria.

* Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Secondary Zones** (Rete - DNS - Zone secondarie) dal menu di navigazione dell'infrastruttura classica.
* Fai clic in qualsiasi punto della **riga che contiene la zona DNS secondaria** per aprire la zona per le modifiche.
  Se esistono più zone secondarie, è possibile filtrare la vista per individuare la zona per cui sono richieste le modifiche.
  {:note}  
* Aggiorna i campi **Master Nameserver** (Server dei nomi master) e **Transfer Interval** (Intervallo di trasferimento) come necessario.
* Seleziona il pulsante **Update** (Aggiorna) per aggiornare la zona DNS secondaria oppure seleziona **Cancel** (Annulla) per annullare l'azione.

## Cosa succede poi
{:#edit-a-secondary-dns-zone-next}

Dopo aver modificato la zona DNS secondaria, i valori **Master Nameserver** (Server dei nomi master) e **Transfer Interval** (Intervallo di trasferimento) rifletteranno l'aggiornamento e la zona secondaria inizierà a ricevere i trasferimenti sulla base delle nuove informazioni. Puoi modificare di nuovo la zona in qualsiasi momento ripetendo la procedura sopra indicata.
