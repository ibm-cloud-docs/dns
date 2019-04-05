---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Come utilizzare l'interfaccia DNS
{:#how-to-use-the-dns-interface}

Attieniti alla seguente procedura per utilizzare l'interfaccia DNS tramite il Portale del cliente di IBM Cloud:

* Vai al [Portale del client ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/).
* Seleziona **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione
* Seleziona **Network->DNS->Forward Zones** (Rete - DNS - Zone di inoltro)
* Seleziona il dominio che vuoi gestire oppure seleziona il pulsante **Add DNS Zone** (Aggiungi zona DNS) sul lato destro della pagina.

## Panoramica dell'interfaccia DNS
{:#dns-interface-overview}
Operare nell'interfaccia DNS nel Portale del cliente ti offre le piene funzionalità per gestire tutti gli aspetti del tuo DNS. Puoi eseguire ogni tipo di gestione di DNS da qualsiasi schermata nell'interfaccia utilizzando la barra dei menu statica nella parte superiore dello schermo.

## Manage DNS (Gestisci DNS)
{:#manage-dns}
Quando raggiungi l'interfaccia DNS nel Portale, verrai instradato direttamente alla schermata **Manage DNS** (Gestisci DNS), che ti consente di visualizzare, modificare o eliminare qualsiasi DNS primario esistente associato al tuo account.

* Per aggiungere nuovi record, ti basta compilare i campi forniti in **Add New Record** (Aggiungi nuovo record) e fare clic sul pulsante **Add Record** (Aggiungi record).
* Per modificare un record esistente, fai clic sulla riga che contiene il record; verrà convertita in modalità di **modifica**. Modifica le impostazioni nei valori desiderati e fai clic su **Update** (Aggiorna).
* Per eliminare un record, seleziona il cerchio rosso a destra del record e fai quindi clic su **Yes** (Sì) al prompt.

## Secondary DNS (DNS secondario)
{:#secondary-dns}

* Vai all'[Infrastruttura classica del portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/).
* Seleziona **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione
* Seleziona **Network->DNS->Secondary Zones** (Rete - DNS - Zone secondarie)

Da questa schermata, puoi aggiungere o modificare impostazioni DNS secondarie.

* Per aggiungere un nuovo record, seleziona **Add Zone** (Aggiungi zona), compila i campi e seleziona **Add** (Aggiungi).
* Per rimuovere un record di DNS secondario, o convertirlo in un record primario, usa l'elenco a discesa **Actions** (Azioni) a destra della pagina e scegli l'opzione appropriata.

## Reverse DNS (DNS inverso)
{:#reverse-dns}

Attieniti alla seguente procedura per utilizzare l'interfaccia DNS tramite la navigazione del Portale:

* Vai all'[Infrastruttura classica del portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/).
* Seleziona **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione
* Seleziona **Network->DNS->Reverse Records** (Rete - DNS - Record inversi)
* Nel menu a discesa, seleziona o immetti l'indirizzo IP per cui desideri modificare il DNS inverso e seleziona quindi **View IP** (Visualizza IP)
  * Per aggiungere il record, immetti il nome host che vuoi utilizzare per la voce di DNS inverso
  * Imposta il TTL (Time-to-live) per il record.
  * Quando sei certo delle informazioni, seleziona **Save** (Salva).

Puoi modificare un'intera sottorete facendo clic su **Edit RDNS for all IPs in this Subnet** (Modifica RDNS per tutti gli IP in questa sottorete) sulla destra della pagina.

* Da questa pagina, seleziona la riga per l'IP che vuoi aggiornare
* Immetti le informazioni nei campi e seleziona quindi **Update** (Aggiorna). Il campo "notes" (note) è facoltativo.

<!--## Propagation Check

* Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network > Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
