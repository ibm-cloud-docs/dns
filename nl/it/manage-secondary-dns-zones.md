---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Gestione delle zone DNS secondarie
{: #manage-secondary-dns-zones}

{{site.data.keyword.cloud}} fornisce un DNS secondario a tutti i clienti come mezzo per memorizzare in cache le zone DNS primarie se si verifica una perdita di dati. Mantenere una zona DNS secondaria non è obbligatorio ma è vivamente consigliato per gli utenti con più domini. 


## Aggiunta di una zona DNS secondaria
{:#add-a-secondary-dns-zone}

Attieniti alla procedura di seguito per aggiungere una zona DNS secondaria:

* Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [{{site.data.keyword.cloud_notm}}portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Secondary Zones** (Rete - DNS - Zone secondarie) dal menu di navigazione dell'infrastruttura classica.
* Seleziona la scheda **Add Zone** (Aggiungi zona).
* Immetti il **dominio per la zona** nel campo **Zone** (Zona).
* Immetti l'**indirizzo IP del server dei nomi master** nel campo **Master Nameserver** (Server dei nomi master).
* Immetti il **tempo di trasferimento** (in minuti) per cui la zona DNS primaria eseguirà il trasferimento alla zona DNS secondaria nel campo **Transfer Interval** (Intervallo di trasferimento).
* Seleziona il pulsante **Add** (Aggiungi) per aggiungere la zona oppure seleziona **Cancel** (Annulla) per annullare l'azione.

### Cosa succede dopo l'aggiunta
{:#add-a-secondary-dns-zone-next}

Dopo essere stata creata, una zona DNS secondaria compare nell'elenco delle zone nella schermata Secondary DNS Zones (Zone DNS secondarie). Il trasferimento di dati dalla zona primaria a quella secondaria si verifica agli intervalli da te specificati quando viene creata la zona. In qualsiasi momento, puoi [modificare](#edit-a-secondary-dns-zone), [trasferire manualmente](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) oppure [convertire](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) la zona in una zona primaria. La zona DNS secondaria può anche essere [eliminata](#delete-a-secondary-dns-zone) in qualsiasi momento.

## Modifica di una zona DNS secondaria
{:#edit-a-secondary-dns-zone}

Le zone DNS secondarie possono essere modificate in qualsiasi momento per aggiornare il server dei nomi master o l'intervallo di trasferimento. Attieniti alla seguente procedura per modificare una zona DNS secondaria.

* Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [{{site.data.keyword.cloud_notm}}portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Secondary Zones** (Rete - DNS - Zone secondarie) dal menu di navigazione dell'infrastruttura classica.
* Fai clic in qualsiasi punto della **riga che contiene la zona DNS secondaria** per aprire la zona per le modifiche.
  Se esistono più zone secondarie, è possibile filtrare la vista per individuare la zona per cui sono richieste le modifiche.
  {:note}  
* Aggiorna i campi **Master Nameserver** (Server dei nomi master) e **Transfer Interval** (Intervallo di trasferimento) come necessario.
* Seleziona il pulsante **Update** (Aggiorna) per aggiornare la zona DNS secondaria oppure seleziona **Cancel** (Annulla) per annullare l'azione.

### Cosa succede dopo la modifica
{:#edit-a-secondary-dns-zone-next}

Dopo aver modificato la zona DNS secondaria, i valori **Master Nameserver** (Server dei nomi master) e **Transfer Interval** (Intervallo di trasferimento) rifletteranno l'aggiornamento e la zona secondaria inizierà a ricevere i trasferimenti sulla base delle nuove informazioni. Puoi modificare di nuovo la zona in qualsiasi momento ripetendo la procedura sopra indicata.

## Eliminazione di una zona DNS secondaria
{:#delete-a-secondary-dns-zone}

Dopo essere stata creata, una zona DNS secondaria può essere eliminata in qualsiasi momento. Tieni presente che, se viene eliminata, una zona DNS secondaria non può essere recuperata. Attieniti alla seguente procedura per eliminare un record DNS secondario.

 * Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [{{site.data.keyword.cloud_notm}}portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Secondary Zones** (Rete - DNS - Zone secondarie) dal menu di navigazione dell'infrastruttura classica.
* Seleziona **Delete** (Elimina) dall'elenco a discesa **Actions** (azioni) per la zona per cui è richiesta l'eliminazione. Verrà visualizzata una casella a comparsa di conferma.
  Se esistono più zone secondarie, è possibile filtrare la vista per individuare la zona da eliminare.
  {:note}
* Seleziona il pulsante **Yes** (Sì) per confermare l'eliminazione oppure seleziona il pulsante **No** per annullare l'azione.

### Cosa succede dopo l'eliminazione
{:#delete-a-secondary-dns-zone-next}

Dopo che una zona DNS secondaria è stata eliminata, i trasferimenti automatizzati dalla zona primaria cesseranno e la zona secondaria non esisterà più. Se in un qualsiasi momento è necessaria una zona DNS secondaria per la zona primaria, [è possibile creare una zona DNS secondaria](#add-a-secondary-dns-zone) nuovamente.
