---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-06"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Domande frequenti sui domini secondari

## Quali server DNS di IBM Cloud risponderanno per i miei domini secondari?

I server DNS autoritari Anycast di IBM Cloud abilitati a IPv6:

 * ns1.softlayer.com
 * ns2.softlayer.com

## Da dove proverranno i trasferimenti di zona?

I trasferimenti dei tuoi domini secondari proverranno da uno dei seguenti quattro indirizzi IP:

  * 66.228.118.67
  * 67.228.119.235
  * 208.43.119.235
  * 12.96.161.249

## Dopo il trasferimento di un dominio, quanto tempo ci vuole perché il dominio o le modifiche a esso apportate diventino visibili?

Il dominio e le eventuali modifiche a esso apportate saranno visibili sui server DNS di IBM Cloud immediatamente dopo il completamento del trasferimento. A causa della natura della memorizzazione in cache e della propagazione di DNS, potrebbe volerci un po' perché tali modifiche siano visibili su altri server DNS.  

## Sono supportate le notifiche di aggiornamento di zona?

Le notifiche non sono attualmente supportate.

## Quanto è immediato il pulsante Transfer Now (Trasferisci ora)?

Dopo che hai fatto clic sul pulsante Transfer Now (Trasferisci ora), il dominio verrà trasferito all'inizio del minuto successivo.

## È possibile configurare un master sulla rete privata o dovrà passare per la rete pubblica?

Non attualmente. Tutte le richieste AXFR vengono effettuate sulla rete pubblica.

## Gli slave vengono rimossi dopo un certo numero di giorni per cui il master non è disponibile?

Smetteremo di tentare il trasferimento di un dominio se il suo master è inattivo o configurato erroneamente per un periodo prolungato. Il portale fornisce un feedback al cliente (la scheda Error Messages (Messaggi di errore)) e un metodo per riattivare un dominio (la scheda Manual Zone Transfer (Trasferimento di zona manuale)) nel caso in cui si verifichino dei problemi durante il trasferimento della zona e ne viene, di conseguenza, eseguita la disabilitazione.

## 1 minuto è la frequenza di trasferimento più bassa?

Sì.

## Se la frequenza è impostata a 1920 minuti, e quindi nuovamente a 10, dovranno scadere i 1920 minuti prima che la nuova frequenza diventi effettiva?

No. Il sistema calcola la coda di ritrasferimento rilevando il tempo del nostro ultimo tentativo di trasferimento e aggiungendo ad esso la frequenza. Quindi, se hai una frequenza impostata a 1920 e la cambi a 10 minuti, ritenteremo immediatamente purché siano trascorsi almeno 10 minuti dal nostro ultimo tentativo di trasferimento e quindi, successivamente, lo faremo ogni 10 minuti.
