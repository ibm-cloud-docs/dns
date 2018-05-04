---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Come utilizzare l'interfaccia DNS

Attieniti alla seguente procedura per utilizzare l'interfaccia DNS tramite il Portale del cliente di IBM Cloud:

* Vai al [Portale del client ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/).
* Seleziona **Network->DNS->Forward Zones** (Rete - DNS - Zone di inoltro)
* Seleziona il dominio che vuoi gestire oppure seleziona il pulsante **Add DNS Zone** (Aggiungi zona DNS) sul lato destro della pagina.

## Panoramica dell'interfaccia DNS
Operare nell'interfaccia DNS nel Portale del cliente ti offre le piene funzionalità per gestire tutti gli aspetti del tuo DNS. Puoi eseguire ogni tipo di gestione di DNS da qualsiasi schermata nell'interfaccia utilizzando la barra dei menu statica nella parte superiore dello schermo.

## Manage DNS (Gestisci DNS)
Quando raggiungi l'interfaccia DNS nel Portale, verrai instradato direttamente alla schermata **Manage DNS** (Gestisci DNS), che ti consente di visualizzare, modificare o eliminare qualsiasi DNS primario esistente associato al tuo account.

* Per aggiungere nuovi record, ti basta compilare i campi forniti in **Add New Record** (Aggiungi nuovo record) e fare clic sul pulsante **Add Record** (Aggiungi record).
* Per modificare un record esistente, fai clic sulla riga che contiene il record; verrà convertita in modalità di **modifica**. Modifica le impostazioni nei valori desiderati e fai clic su **Update** (Aggiorna).
* Per eliminare un record, seleziona il cerchio rosso a destra del record e fai quindi clic su **Yes** (Sì) al prompt.

## Secondary DNS (DNS secondario)

* Vai al [Portale del client ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/).
* Seleziona **Network->DNS->Secondary Zones** (Rete - DNS - Zone secondarie)

Da questa schermata, puoi aggiungere o modificare impostazioni DNS secondarie.

* Per aggiungere un nuovo record, seleziona **Add Zone** (Aggiungi zona), compila i campi e seleziona **Add** (Aggiungi).
* Per rimuovere un record di DNS secondario, o convertirlo in un record primario, usa l'elenco a discesa **Actions** (Azioni) a destra della pagina e scegli l'opzione appropriata.

## Reverse DNS (DNS inverso)

Attieniti alla seguente procedura per utilizzare l'interfaccia DNS tramite la navigazione del Portale:

* Vai al [Portale del client ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/).
* Seleziona **Network->DNS->Reverse Records** (Rete - DNS - Record inversi)
* Nel menu a discesa, seleziona o immetti l'indirizzo IP per cui desideri modificare il DNS inverso e seleziona quindi **View IP** (Visualizza IP)
  * Per aggiungere il record, immetti il nome host che vuoi utilizzare per la voce di DNS inverso
  * Imposta il TTL (Time-to-live) per il record.
  * Quando sei certo delle informazioni, seleziona **Save** (Salva).

Puoi modificare un'intera sottorete facendo clic su **Edit RDNS for all IPs in this Subnet** (Modifica RDNS per tutti gli IP in questa sottorete) sulla destra della pagina.

* Da questa pagina, seleziona la riga per l'IP che vuoi aggiornare
* Immetti le informazioni nei campi e seleziona quindi **Update** (Aggiorna). Il campo "notes" (note) è facoltativo.

## Controllo della propagazione

* Vai al [Portale del client ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/).
* Seleziona **Network->Tools** (Rete-Strumenti)

Nella pagina che viene caricata, puoi selezionare da più strumenti; per controllare la propagazione del tuo nome dominio nei server DNS, utilizza l'opzione nella parte inferiore.

* Immetti le informazioni appropriate nei campi e seleziona quindi **Check DNS** (Controlla DNS)
* Dopo alcuni istanti, la casella sulla destra verrà aggiornata con le informazioni DNS attuali per il dominio.
