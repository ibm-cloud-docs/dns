---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Aggiunta o modifica di un record PTR (puntatore)

I record PTR, o puntatore, risolvono gli indirizzi IP in nomi host. Gli utenti possono aggiungere dei record PTR da associare a un indirizzo IP utilizzando la funzione di DNS inverso nel [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){:new_window}. Inoltre, i record PTR possono essere modificati nello stesso modo in cui vengono aggiunti. Attieniti alla seguente procedura per aggiungere o modificare un record PTR per un dispositivo:

1. Richiama l'**indirizzo IP pubblico** per il dispositivo che riceverà il record PTR dall'**elenco dispositivi**.
* Visualizza la schermata **Reverse DNS Records** (Record DNS inverso). Fai riferimento a [Using the DNS Zones Screen](use-dns-zones-screen.html) (Utilizzo della schermata DNS Zones (Zone DNS)).
* Immetti l'**indirizzo IP pubblico** richiamato dall'elenco dispositivi nel campo **View IP** (Visualizza IP).
* Fai clic in qualsiasi punto della riga che contiene i dettagli del **record inverso** per aprire la riga per le modifiche.
* Completa o aggiorna i campi per il record in base alla tabella che segue:<br/><br/><table border="1"><tbody><tr><th>Campo</th><th>Immissione</th></tr><tr><td>Reverse DNS (DNS inverso)</td><td>Il nome host in cui verrà risolto l'indirizzo IP.</td></tr><tr><td>Reverse TTL (TTL inverso)</td><td>Il TTL (Time-to-live) per il nuovo record</td></tr><tr><td>Notes (Note)</td><td>Qualsiasi nota applicabile relativa al record</td></tr></tbody></table><br/>
* Fai clic sul pulsante **Update** (Aggiorna) per aggiornare il record. Fai clic su **Cancel** (Annulla) per annullare l'azione.

## Cosa succede poi

Dopo che è stato aggiunto un record PTR, l'indirizzo IP pubblico associato a tale record verrà risolto nel nome host specificato nel record. Il record può essere modificato in qualsiasi momento. Per rimuovere i dettagli dal record PTR, elimina tutte le informazioni dai campi utilizzando il processo **Edit** (Modifica).
