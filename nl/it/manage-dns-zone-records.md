---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone Record, Update DNS Zone Record, edit dns zone record, add dns zone record, delete dns zone record 

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

# Gestione dei record di zona DNS
{: #manage-dns-zone-records}
Questa sezione fornisce i dettagli su come aggiungere, modificare ed eliminare i record di zona DNS.

## Aggiunta di un record di zona DNS
{: #add-a-dns-zone-record}

Dopo aver [aggiunto una zona DNS](/docs/infrastructure/dns?topic=dns-manage-dns-zones#add-a-dns-zone), è possibile aggiungere ad essa dei record in qualsiasi momento. Tali record includono:

* Record A (Host)
* Record AAAA (Host)
* Record CNAME (Alias)
* Record MX (Mail Exchange)
* Record TXT (Text)
* Record SRV (Service)

Attieniti alla seguente procedura per aggiungere un record di zona DNS:

* Vai alla schermata **DNS Zone** (Zona DNS). Fai riferimento a [Using the DNS Zones Screen](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) (Utilizzo della schermata DNS Zones (Zone DNS)).
* Seleziona la zona DNS a cui verrà aggiunto il record.
* Seleziona il **tipo di risorsa** desiderato dall'elenco a discesa **Resource Type** (Tipo di risorsa).
* Completa i restanti campi per il nuovo record. Fai riferimento alla tabella di seguito per ulteriori informazioni: <br/><br/><table border="1"><tbody><tr><th scope="col">Tipo di record</th><th scope="col">Campo</th><th scope="col">Immissione</th></tr><tr><td rowspan="3">A (Host), AAAA (Host) o CNAME (Alias)</td><td>Host</td><td>Immetti il <strong>nome host</strong>.</td></tr><tr><td>Points To (Punta a)</td><td>Immetti l'<strong>indirizzo IP</strong> a cui punta il record host.</td></tr><tr><td>TTL</td><td>Seleziona il TTL (Time-to-live) dall'elenco a discesa. Il TTL, per impostazione predefinita, è di 15 minuti.</td></tr><tr><td rowspan="4">MX (Mail Exchange)</td><td>Priority (Priorità)</td><td>Immetti la <strong>priorità</strong> dell'host di destinazione. Più basso è il numero e più alta è la priorità.</td></tr><tr><td>Host</td><td>Immetti il <strong>nome host</strong>.</td></tr><tr><td>Goes (Destinazione)</td><td>Immetti il <strong>CNAME</strong> del server di posta. Viene di norma rappresentato come `mail.example.com`.</td></tr><tr><td>TTL</td><td>Seleziona il TTL (Time-to-live) dall'elenco a discesa. Il TTL, per impostazione predefinita, è di 15 minuti.</td></tr><tr><td rowspan="3">TXT (Text)</td><td>Name (Nome)</td><td>Immetti <strong>@</strong> o il <strong>nome dominio</strong>.</td></tr><tr><td>Value (Valore)</td><td>Immetti il <strong>record</strong> per verificare gli appropriati diritti di email per un dominio o un IP.</td></tr><tr><td>TTL</td><td>Seleziona il TTL (Time-to-live) dall'elenco a discesa. Il TTL, per impostazione predefinita, è di 15 minuti.</td></tr><tr><td rowspan="8">SRV (Service Record)</td><td>Service (Servizio)</td><td>Immetti il <strong>nome simbolico</strong> del servizio desiderato.</td></tr><tr><td>Protocol (Protocollo)</td><td>Seleziona il <strong>protocollo</strong> utilizzato dall'elenco a discesa.</td></tr><tr><td>Priority (Priorità)</td><td>Immetti la <strong>priorità</strong> dell'host di destinazione. Più basso è il numero e più alta è la priorità.</td></tr><tr><td>Weight (Peso)</td><td>Immetti il <strong>peso relativo</strong> per i record con la stessa priorità.</td></tr><tr><td>Port (Porta)</td><td>Immetti la <strong>porta TCP o UPD</strong> su cui deve essere trovato il servizio.</td></tr><tr><td>Host (optional) (Host (facoltativo))</td><td>Immetti il <strong>nome host</strong> per il servizio.</td></tr><tr><td>Target (Destinazione)</td><td>Immetti il <strong>nome host canonico</strong> della macchina che fornisce il servizio.</td></tr><tr><td>TTL</td><td>Seleziona il TTL (Time-to-live) dall'elenco a discesa. Il TTL, per impostazione predefinita, è di 15 minuti.</td></tr></tbody></table><br/>
* Seleziona il pulsante **Add Record** (Aggiungi record) per aggiungere il nuovo record di zona.

### Cosa succede poi
{:#add-a-dns-zone-record-next}

Dopo che l'hai aggiunto, il record di zona compare nella sezione **Existing Records** (Record esistenti) dello schermo. Puoi [modificare](#edit-a-dns-zone-record) o [eliminare](#delete-a-dns-zone-record) il record di zona in qualsiasi momento.

## Modifica di un record di zona DNS
{: #edit-a-dns-zone-record}

I record di zona DNS esistenti possono essere modificati da un utente per aggiornare diverse aree, quali TTL (Time-to-live) record PTR (puntatore) e nomi host. In un qualsiasi momento, a un record di zona DNS possono essere associati più host e alias. Attieniti alla procedura di seguito per modificare un record di zona DNS esistente.

* Vai alla schermata **DNS Zone** (Zona DNS) desiderata selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Forward Zones** (Rete - DNS - Zone di inoltro) dal menu di navigazione dell'infrastruttura classica.
* Fai clic sulla **riga** che contiene qualsiasi record esistente. 

  I record in corsivo non possono essere modificati. Ciò è di norma limitato ai record server dei nomi (NS, name server).
  {: note}
  
* Aggiorna i dettagli del record come necessario.
* Seleziona il pulsante **Update** (Aggiorna) per aggiornare il record oppure seleziona **Cancel** (Annulla) per annullare l'azione.

### Cosa succede poi
{: #edit-a-dns-zone-record-next}

Quando il record viene aggiornato, i relativi dettagli presenteranno automaticamente la nuova voce. I record possono essere aggiornati in qualsiasi momento ed è possibile eliminare quelli esistenti e [aggiungerne](#add-a-dns-zone-record) di nuovi.

## Eliminazione di un record di zona DNS
{: #delete-a-dns-zone-record}

L'eliminazione di un record di zona DNS viene eseguita tramite la schermata **DNS Edit Zone** (Modifica zona DNS) . L'eliminazione di un record di zona DNS non può essere annullata.
* Seleziona la zona DNS che ha il record che vuoi eliminare facendo clic sul nome nell'elenco di zone DNS.
* Seleziona l'icona di eliminazione alla fine della riga che contiene il record desiderato. Viene visualizzata una casella a comparsa di conferma.
* Seleziona il pulsante **Yes** (Sì) per confermare l'eliminazione oppure seleziona il pulsante **No** per annullare l'azione.
