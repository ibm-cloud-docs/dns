---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Terminologia di DNS

## Memorizzazione in cache e TTL (Time-to-live)

A causa dell'elevato volume di richieste generato da un sistema come DNS, i progettisti hanno fornito un meccanismo per ridurre il carico sui singoli server DNS nel seguente modo:

Quando un resolver DNS (ossia un client) riceve una risposta DNS, memorizza in cache tale risposta per uno specifico periodo di tempo, detto TTL (Time-to-live). Il valore di TTL è impostato dall'amministratore del server DNS che fornisce la risposta. Dopo che la risposta è finita in cache, il resolver consulta la sua risposta in cache (memorizzata); solo quando il TTL scade (o quando l'amministratore elimina manualmente la risposta dalla memoria del resolver) il resolver contatterà il server DNS per le stesse informazioni.

## Parametri del record SOA (Start of Authority)

Di norma, il TTL (Time-to-live) viene specificato nel record SOA (Start of Authority). I parametri SOA sono:

### Serial (Di serie)

Il numero di revisione di questo file di zona. Aumenta questo numero ogni volta che il file di zona viene modificato in modo che le modifiche vengano distribuite agli eventuali server DNS secondari.

### Refresh (Aggiorna)

La quantità di tempo, in secondi, per cui un server dei nomi secondario deve attendere per controllare la presenza di una copia nuova di una zona DNS dal server dei nomi primario del dominio. Se un file di zona ha subito delle modifiche, il server DNS aggiornerà la sua copia della zona in modo che corrisponda alla zona del server DNS primario.

### Retry (Ritenta)

La quantità di tempo, in secondi, per cui, se un tentativo di aggiornamento da parte di un server dei nomi secondario non è riuscito, uno o più server dei nomi primari del dominio devono attendere prima di tentare nuovamente un aggiornamento della zona di un dominio con tale server dei nomi secondario.

### Expire (Scade)

La quantità di tempo, in secondi, per cui uno o più server dei nomi secondari terrà una zona prima che non venga più considerata autorevole.

### Minimum (Minimo)

La quantità di tempo, in secondi, per cui i record di risorsa di un dominio sono validi. Questo è noto anche come TTL minimo e può essere sovrascritto dal TTL del record di una singola risorsa.

### TTL (Time-to-live)

Il numero di secondi per cui un nome dominio viene memorizzato in cache localmente prima della scadenza e del ritorno ai server dei nomi autoritari per le informazioni aggiornate.
