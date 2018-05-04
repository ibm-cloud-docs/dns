---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Aggiornamento di un record di DNS inverso

DNS inverso consente agli utenti di identificare il dominio che è associato a un indirizzo IP. I clienti possono aggiornare i loro record di DNS inverso in qualsiasi momento per modificare PTR e TTL (Time-to-live). Nella versione **Manage** (Gestione) del [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/), puoi aggiornare i record PTR in blocco utilizzando lo strumento **Search and Replace** (Cerca e sostituisci). Questo strumento ti consente di immettere, parzialmente o integralmente, il PTR nel campo Search (Ricerca) e sostituire ciascuna ricorrenza nei PTR corrispondenti con le informazioni desiderate. 

Nota: questo strumento funziona solo quando i PTR esistenti sono associati al server o alla VLAN. Se non esiste alcun PTR, non viene elencato alcun dettaglio e i tentativi di aggiornamento produrranno un errore. 

Per aggiungere un record PTR di DNS inverso, consulta [Aggiunta e modifica di un record PTR (puntatore)](add-and-edit-ptr-pointer-record.html). Attieniti alla seguente procedura per aggiornare un record di DNS inverso:

 * Vai al [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) utilizzando le tue credenziali univoche.
 * Seleziona **DNS** dal menu a discesa **Network** (Rete).
 * Seleziona l'opzione di menu **Reverse DNS** (DNS inverso).
 * Determina se l'aggiornamento deve essere effettuato per tutta la VLAN di rete degli indirizzi IP corrispondente oppure se le modifiche devono essere apportate a un singolo IP.<br><br><table border="1"><tbody><tr><th>Se l'aggiornamento verrà effettuato per...</th><th>Allora...</th></tr><tr><td>Singolo IP</td><td><ul><li>Seleziona il <b>menu a discesa</b> per visualizzare gli indirizzi IP</li><li>Fai clic sull'<strong>indirizzo IP</strong> desiderato per visualizzare i dettagli del DNS inverso associati al server.</li></ul></td></tr><tr><td>Tutti gli indirizzi IP corrispondenti sulla VLAN di rete</td><td><ul><li>Seleziona l'opzione <strong>View IP</strong> (Visualizza IP) dopo aver selezionato un IP come indicato in precedenza.</li><li>Seleziona l'opzione <strong>Edit RDNS for all IPs in this Subnet</strong> (Modifica RDNS per tutti gli IP in questa sottorete).</li></ul></td></tr></tbody></table><br/>
 * Per i singoli IP, ti basta aggiungere **nome host** e il **TTL inverso** e selezionare quindi **Save** (Salva). Per l'intera **Subnet** (Sottorete), evidenzia lo spazio aperto sotto la colonna **Reverse DNS** (DNS inverso) e aggiungi il **nome host** e seleziona quindi il pulsante **Update** (Aggiorna). Questa attività dovrà essere eseguita per ogni indirizzo IP nella sottorete.
