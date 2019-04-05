---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Update DNS Zone Record, edit dns zone record

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Modifica di un record di zona DNS
{:#edit-a-dns-zone-record}

I record di zona DNS esistenti possono essere modificati da un utente per aggiornare diverse aree, quali TTL (Time-to-live) record PTR (puntatore) e nomi host. In un dato momento, a un record di zona DNS possono essere associati più host e alias. Attieniti alla procedura di seguito per modificare un record di zona DNS esistente.

* Vai alla schermata **DNS Zone** (Zona DNS) desiderata selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Forward Zones** (Rete - DNS - Zone di inoltro) dal menu di navigazione dell'infrastruttura classica.
* Fai clic sulla **riga** che contiene qualsiasi record esistente. **Nota:** i record presentati in corsivo non sono disponibili per la modifica. Ciò è di norma limitato ai record server dei nomi (NS, name server).
* Aggiorna i dettagli del record come necessario.
* Seleziona il pulsante **Update** (Aggiorna) per aggiornare il record oppure seleziona **Cancel** (Annulla) per annullare l'azione.

## Cosa succede poi
{:#edit-a-dns-zone-record-next}

Quando il record viene aggiornato, i relativi dettagli presenteranno automaticamente la nuova voce. I record possono essere aggiornati in qualsiasi momento ed è possibile eliminare quelli esistenti e [aggiungerne](/docs/infrastructure/dns?topic=dns-add-a-dns-zone-record) di nuovi.
