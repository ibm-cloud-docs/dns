---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone, DNS management, Add DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Aggiunta di una zona DNS
{:#add-a-dns-zone}

La gestione DNS di {{site.data.keyword.BluSoftlayer_notm}} si estende alle zone DNS che potrebbero non trovarsi nella rete {{site.data.keyword.BluSoftlayer_notm}}. Utilizzando la nostra interfaccia, puoi aggiungere zone DNS in qualsiasi momento, come un singolo dominio oppure in blocco. L'aggiunta di zone DNS attualmente avviene nella versione [Control](https://control.softlayer.com/) (Controllo) del Portale del cliente. Attieniti alla seguente procedura per aggiungere una o più zone DNS

* Accedi alla versione [Control](https://control.softlayer.com/) (Controllo) del Portale del cliente utilizzando le tue credenziali univoche.
* Seleziona **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione
* Seleziona **DNS** dal menu a discesa **Network** (Rete).
* Seleziona **Forward Zones** (Zone di inoltro).
* Seleziona la scheda **Add DNS Zone** (Aggiungi zona DNS) nell'angolo superiore destro.
* Determina se stai aggiungendo un singolo dominio o più domini:<br> <br><table border="1"><tbody><tr><th>Se stai aggiungendo...</th><th>Allora...</th></tr><tr><td>Un singolo dominio</td><td>Completa la seguente procedura nella sezione <strong>Add single domain</strong> (Aggiungi singolo dominio) dello schermo:<br> <ul><li>Immetti il <strong>nome dominio</strong> nel campo <strong>Domain Name</strong> (Nome dominio).</li><li>Immetti l'<strong>indirizzo IP</strong> a cui punterà il nome dominio nel campo <strong>IP Address</strong> (Indirizzo IP).</li><li>Fai clic sul pulsante <strong>Add Zone</strong> (Aggiungi zona) per aggiungere il dominio.<br> </li></ul></td></tr><tr><td>Più domini</td><td>Determina se i domini saranno associati a un singolo indirizzo IP o a più IP:<br> <p> </p><p> </p><p> </p><p> </p><ul><li>Se i domini saranno associati a un singolo indirizzo IP,<ul><li>Immetti <strong>ciascun dominio</strong> nella casella di testo <strong>Domains</strong> (Domini).</li><li>Immetti l'<strong>indirizzo IP</strong> nel campo <strong>Default IP Address</strong> (Indirizzo IP predefinito).</li><li>Fai clic sul pulsante <strong>Add Zone</strong> (Aggiungi zona) per aggiungere i domini in blocco.</li></ul></li><li>Se i domini saranno associati a più indirizzi IP,<ul><li>Immetti <strong>ciascun dominio</strong> e il suo corrispondente <strong>indirizzo IP</strong> come un elemento a singola riga nella casella di testo <strong>Domains</strong> (Domini).</li><li>Fai clic sul pulsante <strong>Add Zone</strong> (Aggiungi zona) per aggiungere i domini in blocco.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## Cosa succede poi
{:#add-a-dns-zone-next}

Dopo essere stata aggiunta, una zona DNS compare nell'elenco di zone DNS nella [schermata DNS Zones](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) (Zone DNS) nel [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). La zona può essere [modificata](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record) o [eliminata](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone) in qualsiasi momento.


