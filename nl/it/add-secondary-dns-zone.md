---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Aggiunta di una zona DNS secondaria

{{site.data.keyword.BluSoftlayer_notm}} fornisce un DNS secondario a tutti i clienti come mezzo per memorizzare in cache le zone DNS primarie se si verifica una perdita di dati. Mantenere una zona DNS secondaria non è obbligatorio ma è vivamente consigliato per gli utenti con più domini. Attieniti alla procedura di seguito per aggiungere una zona DNS secondaria:

* Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Fai riferimento a [Using the DNS Zones Screen](use-dns-zones-screen.html){:new_window} (Utilizzo della schermata DNS Zones (Zone DNS)).
* Seleziona la scheda **Add Zone** (Aggiungi zona).
* Immetti il **dominio per la zona** nel campo **Zone** (Zona).
* Immetti l'**indirizzo IP del server dei nomi master** nel campo **Master Nameserver** (Server dei nomi master).
* Immetti il **tempo di trasferimento** (in minuti) per cui la zona DNS primaria eseguirà il trasferimento alla zona DNS secondaria nel campo **Transfer Interval** (Intervallo di trasferimento).
* Seleziona il pulsante **Add** (Aggiungi) per aggiungere la zona oppure seleziona **Cancel** (Annulla) per annullare l'azione.

## Cosa succede poi

Dopo essere stata creata, una zona DNS secondaria compare nell'elenco delle zone nella schermata Secondary DNS Zones (Zone DNS secondarie). Il trasferimento di dati dalla zona primaria a quella secondaria si verifica agli intervalli da te specificati quando viene creata la zona. In qualsiasi momento, puoi [modificare](edit-secondary-dns-zone.html), [trasferire manualmente](make-manual-zone-transfer-secondary-dns.html) oppure [convertire](convert-secondary-dns-zone-primary-zone.html) la zona in una zona primaria. La zona DNS secondaria può anche essere [eliminata](delete-secondary-dns-zone.html) in qualsiasi momento.
