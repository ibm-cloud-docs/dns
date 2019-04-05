---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone Record, TTL Select, Relative Weight

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Aggiunta di un record di zona DNS
{:#add-a-dns-zone-record}

Dopo aver [aggiunto una zona DNS](/docs/infrastructure/dns?topic=dns-add-a-dns-zone), è possibile aggiungere ad essa dei record in qualsiasi momento. Tali record includono:

* Record A (Host)
* Record AAAA (Host)
* Record CNAME (Alias)
* Record MX (Mail Exchange)
* Record TXT (Text)
* Record SRV (Service)

Attieniti alla seguente procedura per aggiungere un record di zona DNS:

* Vai alla schermata **DNS Zone** (Zona DNS) desiderata. Fai riferimento a [Using the DNS Zones Screen](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) (Utilizzo della schermata DNS Zones (Zone DNS)).
* Seleziona la zona DNS a cui verrà aggiunto il record.
* Seleziona il **tipo di risorsa** desiderato dall'elenco a discesa **Resource Type** (Tipo di risorsa).
* Completa i restanti campi per il nuovo record. Consulta la tabella di seguito per ulteriori informazioni:<br/><br/><table border="1"><tbody><tr><th scope="col">Tipo di record</th><th scope="col">Campo</th><th scope="col">Immissione</th></tr><tr><td rowspan="3">A (Host), AAAA (Host) o CNAME (Alias)</td><td>Host</td><td>Immetti il <strong>nome host</strong>.</td></tr><tr><td>Points To (Punta a)</td><td>Immetti l'<strong>indirizzo IP</strong> a cui punta il record host.</td></tr><tr><td>TTL</td><td>Seleziona il TTL (Time-to-live) dall'elenco a discesa. Il TTL, per impostazione predefinita, è di 15 minuti.</td></tr><tr><td rowspan="4">MX (Mail Exchange)</td><td>Priority (Priorità)</td><td>Immetti la <strong>priorità</strong> dell'host di destinazione. Più basso è il numero e più alta è la priorità.</td></tr><tr><td>Host</td><td>Immetti il <strong>nome host</strong>.</td></tr><tr><td>Goes (Destinazione)</td><td>Immetti il <strong>CNAME</strong> del server di posta. Viene di norma rappresentato come mail.example.com.</td></tr><tr><td>TTL</td><td>Seleziona il TTL (Time-to-live) dall'elenco a discesa. Il TTL, per impostazione predefinita, è di 15 minuti.</td></tr><tr><td rowspan="3">TXT (Text)</td><td>Name (Nome)</td><td>Immetti <strong>@</strong> o il <strong>nome dominio</strong>.</td></tr><tr><td>Value (Valore)</td><td>Immetti il <strong>record</strong> per verificare gli appropriati diritti di email per un dominio o un IP.</td></tr><tr><td>TTL</td><td>Seleziona il TTL (Time-to-live) dall'elenco a discesa. Il TTL, per impostazione predefinita, è di 15 minuti.</td></tr><tr><td rowspan="8">SRV (Service Record)</td><td>Service (Servizio)</td><td>Immetti il <strong>nome simbolico</strong> del servizio desiderato.</td></tr><tr><td>Protocol (Protocollo)</td><td>Seleziona il <strong>protocollo</strong> utilizzato dall'elenco a discesa.</td></tr><tr><td>Priority (Priorità)</td><td>Immetti la <strong>priorità</strong> dell'host di destinazione. Più basso è il numero e più alta è la priorità.</td></tr><tr><td>Weight (Peso)</td><td>Immetti il <strong>peso relativo</strong> per i record con la stessa priorità.</td></tr><tr><td>Port (Porta)</td><td>Immetti la <strong>porta TCP o UPD</strong> su cui deve essere trovato il servizio.</td></tr><tr><td>Host (optional) (Host (facoltativo))</td><td>Immetti il <strong>nome host</strong> per il servizio.</td></tr><tr><td>Target (Destinazione)</td><td>Immetti il <strong>nome host canonico</strong> della macchina che fornisce il servizio.</td></tr><tr><td>TTL</td><td>Seleziona il TTL (Time-to-live) dall'elenco a discesa. Il TTL, per impostazione predefinita, è di 15 minuti.</td></tr></tbody></table><br/>
* Seleziona il pulsante **Add Record** (Aggiungi record) per aggiungere il nuovo record di zona.

## Cosa succede poi
{:#add-a-dns-zone-record-next}

Dopo che l'hai aggiunto, il record di zona compare nella sezione **Existing Records** (Record esistenti) dello schermo. Puoi [modificare](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record) o [eliminare](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone) il record di zona in qualsiasi momento.
