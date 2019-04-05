---
copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-02-26"

keywords: Reverse DNS Record, Reverse DNS, IP address, Individual IP Select

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Aggiornamento di un record di DNS inverso
{:#update-reverse-dns-record}

DNS inverso consente agli utenti di identificare il dominio che è associato a un indirizzo IP. I clienti possono aggiornare i loro record di DNS inverso in qualsiasi momento per modificare PTR e TTL (Time-to-live). Nella versione **Manage** (Gestione) della [Console IBM Cloud ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/), puoi aggiornare i record PTR in blocco utilizzando lo strumento **Search and Replace** (Cerca e sostituisci). Questo strumento ti consente di immettere, parzialmente o integralmente, il PTR nel campo Search (Ricerca) e sostituire ciascuna ricorrenza nei PTR corrispondenti con le informazioni desiderate. 

Nota: questo strumento funziona solo quando i PTR esistenti sono associati al server o alla VLAN. Se non esiste alcun PTR, non viene elencato alcun dettaglio e i tentativi di aggiornamento produrranno un errore. 

Per aggiungere un record PTR di DNS inverso, consulta [Aggiunta e modifica di un record PTR (puntatore)](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record). Attieniti alla seguente procedura per aggiornare un record di DNS inverso:

 * Vai alla [Console IBM Cloud ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) utilizzando le tue credenziali univoche.
 * Seleziona **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione.
 * Seleziona **Network > DNS > Reverse DNS** (Rete - DNS - DNS inverso) dal menu di navigazione dell'infrastruttura classica.
 * Digita l'indirizzo IP o selezionalo dal menu a discesa e fai clic su **View IP** (Visualizza IP).
 * Modifica le opzioni elencate e fai clic su **Save** (Salva). Puoi anche scegliere l'opzione **Edit RDNS for all IPs in this Subnet** (Modifica RDNS per tutti gli IP in questa sottorete) per apportare modifiche nell'intera sottorete. 
 

