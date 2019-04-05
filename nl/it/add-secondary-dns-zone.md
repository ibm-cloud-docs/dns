---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, IBM Cloud, Add Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Aggiunta di una zona DNS secondaria
{:#add-a-secondary-dns-zone}

{{site.data.keyword.BluSoftlayer_notm}} fornisce un DNS secondario a tutti i clienti come mezzo per memorizzare in cache le zone DNS primarie se si verifica una perdita di dati. Mantenere una zona DNS secondaria non è obbligatorio ma è vivamente consigliato per gli utenti con più domini. Attieniti alla procedura di seguito per aggiungere una zona DNS secondaria:

* Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Secondary Zones** (Rete - DNS - Zone secondarie) dal menu di navigazione dell'infrastruttura classica.
* Seleziona la scheda **Add Zone** (Aggiungi zona).
* Immetti il **dominio per la zona** nel campo **Zone** (Zona).
* Immetti l'**indirizzo IP del server dei nomi master** nel campo **Master Nameserver** (Server dei nomi master).
* Immetti il **tempo di trasferimento** (in minuti) per cui la zona DNS primaria eseguirà il trasferimento alla zona DNS secondaria nel campo **Transfer Interval** (Intervallo di trasferimento).
* Seleziona il pulsante **Add** (Aggiungi) per aggiungere la zona oppure seleziona **Cancel** (Annulla) per annullare l'azione.

## Cosa succede poi
{:#add-a-secondary-dns-zone-next}

Dopo essere stata creata, una zona DNS secondaria compare nell'elenco delle zone nella schermata Secondary DNS Zones (Zone DNS secondarie). Il trasferimento di dati dalla zona primaria a quella secondaria si verifica agli intervalli da te specificati quando viene creata la zona. In qualsiasi momento, puoi [modificare](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record), [trasferire manualmente](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) oppure [convertire](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) la zona in una zona primaria. La zona DNS secondaria può anche essere [eliminata](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone) in qualsiasi momento.
