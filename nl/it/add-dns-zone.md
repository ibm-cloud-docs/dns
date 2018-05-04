---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Aggiunta di una zona DNS

La gestione DNS di {{site.data.keyword.BluSoftlayer_notm}} si estende alle zone DNS che potrebbero non trovarsi nella rete {{site.data.keyword.BluSoftlayer_notm}}. Utilizzando la nostra interfaccia, puoi aggiungere zone DNS in qualsiasi momento, come un singolo dominio oppure in blocco. L'aggiunta di zone DNS attualmente avviene nella versione [Control](https://control.softlayer.com/) (Controllo) del Portale del cliente. Attieniti alla seguente procedura per aggiungere una o più zone DNS

* Accedi alla versione [Control](https://control.softlayer.com/) (Controllo) del Portale del cliente utilizzando le tue credenziali univoche.
* Seleziona **DNS** dal menu a discesa **Network** (Rete).
* Seleziona **Forward Zones** (Zone di inoltro).
* Seleziona la scheda **Add DNS Zone** (Aggiungi zona DNS) nell'angolo superiore destro.
* Determina se stai aggiungendo un singolo dominio o più domini:<br> <br><table border="1"><tbody><tr><th>Se stai aggiungendo...</th><th>Allora...</th></tr><tr><td>Un singolo dominio</td><td>Completa la seguente procedura nella sezione <strong>Add single domain</strong> (Aggiungi singolo dominio) dello schermo:<br> <ul><li>Immetti il <strong>nome dominio</strong> nel campo <strong>Domain Name</strong> (Nome dominio).</li><li>Immetti l'<strong>indirizzo IP</strong> a cui punterà il nome dominio nel campo <strong>IP Address</strong> (Indirizzo IP).</li><li>Fai clic sul pulsante <strong>Add Zone</strong> (Aggiungi zona) per aggiungere il dominio.<br> </li></ul></td></tr><tr><td>Più domini</td><td>Determina se i domini saranno associati a un singolo indirizzo IP o a più IP:<br> <p> </p><p> </p><p> </p><p> </p><ul><li>Se i domini saranno associati a un singolo indirizzo IP,<ul><li>Immetti <strong>ciascun dominio</strong> nella casella di testo <strong>Domains</strong> (Domini).</li><li>Immetti l'<strong>indirizzo IP</strong> nel campo <strong>Default IP Address</strong> (Indirizzo IP predefinito).</li><li>Fai clic sul pulsante <strong>Add Zone</strong> (Aggiungi zona) per aggiungere i domini in blocco.</li></ul></li><li>Se i domini saranno associati a più indirizzi IP,<ul><li>Immetti <strong>ciascun dominio</strong> e il suo corrispondente <strong>indirizzo IP</strong> come un elemento a singola riga nella casella di testo <strong>Domains</strong> (Domini).</li><li>Fai clic sul pulsante <strong>Add Zone</strong> (Aggiungi zona) per aggiungere i domini in blocco.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## Cosa succede poi

Dopo essere stata aggiunta, una zona DNS compare nell'elenco di zone DNS nella [schermata DNS Zones](access-dns-zones-screen.html) (Zone DNS) nel [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). La zona può essere [modificata](edit-dns-zone-record.html) o [eliminata](delete-dns-zone.html) in qualsiasi momento.
