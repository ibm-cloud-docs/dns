---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Gestione delle zone DNS
{: #manage-dns-zones}

## Aggiunta di una zona DNS
{: #add-a-dns-zone}

La gestione DNS di {{site.data.keyword.cloud}} si estende alle zone DNS che potrebbero non trovarsi nella rete {{site.data.keyword.cloud_notm}}. Utilizzando la nostra interfaccia, puoi aggiungere zone DNS in qualsiasi momento, come un singolo dominio oppure in blocco. L'aggiunta di zone DNS attualmente avviene nella [console di IBM Cloud](https://{DomainName}/). Attieniti alla seguente procedura per aggiungere una o più zone DNS.

* Accedi alla [console di IBM Cloud](https://{DomainName}/) utilizzando le tue credenziali univoche.
* Seleziona **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione
* Seleziona **DNS** dal menu a discesa **Network** (Rete).
* Seleziona **Forward Zones** (Zone di inoltro).
* Seleziona la scheda **Add DNS Zone** (Aggiungi zona DNS) nell'angolo superiore destro.
* Determina se stai aggiungendo un singolo dominio o più domini:

|Se stai aggiungendo...|Allora...|
|---|---|
|Un singolo dominio|Completa la seguente procedura nella sezione **Add single domain** (Aggiungi singolo dominio) dello schermo:<ul><li>Immetti il **nome dominio** nel campo **Domain Name** (Nome dominio).</li><li>Immetti l'**indirizzo IP** a cui punterà il nome dominio nel campo **IP Address** (Indirizzo IP).</li><li>Fai clic sul pulsante **Add Zone** (Aggiungi zona) per aggiungere il dominio.</li></ul>|
|Domini multipli|Determina se i domini saranno associati a un singolo indirizzo IP o a più IP:<ul><li>Se i domini saranno associati a un singolo indirizzo IP,<ul><li>Immetti **ciascun dominio** nella casella di testo **Domains** (Domini).</li><li>Immetti l'**indirizzo IP** nel campo **Default IP Address** (Indirizzo IP predefinito).</li><li>Fai clic sul pulsante **Add Zone** (Aggiungi zona) per aggiungere i domini in blocco.</li></ul></li><li>Se i domini saranno associati a più indirizzi IP,<ul><li>Immetti **ciascun dominio** e il suo corrispondente **indirizzo IP** come un elemento a singola riga nella casella di testo **Domains** (Domini).</li><li>Fai clic sul pulsante **Add Zone** (Aggiungi zona) per aggiungere i domini in blocco.</li></ul></li></ul>


### Cosa succede poi
{:#add-a-dns-zone-next}

Dopo aver aggiunto correttamente una singola zona, vieni automaticamente reindirizzato alla pagina Zone Edit (modifica zona).
Le nuove zone DNS vengono visualizzato nell'elenco delle zone DNS nella [schermata DNS Zones (Zone DNS)](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) nella [console di IBM Cloud![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). La zona può essere [modificata](#edit-a-dns-zone) o [eliminata](#delete-a-dns-zone) in qualsiasi momento.

## Modifica una zona DNS
{: edit-a-dns-zone}
Seleziona la zona DNS che vuoi modificare dall'elenco di zone nella schermata DNS Zones (Zone DNS) facendo clic sul nome della zona. Questo apre la pagina DNS Edit Zone (Modifica zona DNS). Da qui, puoi apportare modifiche alla zona DNS e fare clic su **Update SOA** (Aggiorna SOA) per eseguire il commit delle modifiche. 

La schermata **Edit a DNS Zone** (Modifica una zona DNS) ti consente di aggiungere dei nuovi record e di modificare i record esistenti per la zona che stai modificando. Da questa schermata puoi anche esportare o eliminare la zona.

### Cosa succede poi
{:#edit-a-dns-zone-next}

Fai clic su **View ALL DNS Zones** (Visualizza tutte le zone DNS) per ritornare all'elenco di zone DNS.


## Eliminazione di una zona DNS
{: #delete-a-dns-zone}

Dopo essere stata aggiunta, una zona DNS può essere eliminata in qualsiasi momento. Le eliminazioni di zone DNS sono permanenti; non possono essere annullate. Attieniti alla seguente procedura per eliminare una zona DNS:

* Vai alla schermata **DNS Zone** (Zona DNS) desiderata selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS** (Rete > DNS) dal menu di navigazione dell'infrastruttura classica e seleziona il tipo di zona di cui hai bisogno.
* Seleziona l'icona **Delete** (Elimina) alla fine della riga che contiene la zona DNS desiderata. Verrà visualizzata una casella a comparsa di conferma.
* Seleziona il pulsante **Yes** (Sì) per confermare l'eliminazione oppure seleziona il pulsante **No** per annullare l'azione.

Le zone possono essere eliminate anche dalla schermata Edit DNS Zones (Modifica zone DNS).
{:tip}

### Cosa succede poi
{:#delete-a-dns-zone-next}

Dopo che è stata eliminata, una zona DNS non può essere più gestita utilizzando la [console di IBM Cloud![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). Per gestire nuovamente nel Dashboard la zona eliminata, è necessario [aggiungerla come una nuova zona](#add-a-dns-zone).
