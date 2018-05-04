---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Creazione di server dei nomi privati in cPanel/WHM

Utilizzando il prodotto cPanel/WHM, puoi creare dei server dei nomi privati in qualsiasi momento. I server dei nomi privati consentono ai server dei nomi associati a un sito web (ad esempio `www.yourdomain.com`) di visualizzare il server dei nomi del sito web (ad esempio `ns1.yourdomain.com`) invece del server dei nomi associato all'host web per il sito web (ad esempio `ns1.webhostdomain.com`). L'aggiunta di un server dei nomi privato a un dominio consente anche di accedere a opzioni aggiuntive per la gestione DNS in cPanel/WHM. Attieniti alla procedura in quest'articolo per creare un server dei nomi privato. Se si verificano dei problemi durante o dopo l'esecuzione di questa procedura, ti invitiamo ad [aprire un ticket](/general/create-ticket.html).

## Denomina il server dei nomi

* Accedi a WHM sul tuo server al seguente URL: http://xx.xx.xx.xx:2086.
* Seleziona **Basic cPanel/WHM Setup** (Configurazione cPanel/WHM) di base) dal menu **Server Configuration** (Configurazione server).
* Immetti il nome o i nomi host di server dei nomi desiderati in uno o più dei seguenti campi:
  * Primary Nameserver (Server dei nomi primario)
  * Secondary Nameserver (Server dei nomi secondario)
  * Tertiary Nameserver (Server dei nomi terziario)
  * Quaternary Nameserver (Server dei nomi quaternario)
* Seleziona il pulsante **Save** (Salva).

## Crea un file di zona per il dominio

* Seleziona **Add a DNS Zone** (Aggiungi una zona DNS) dal menu **DNS Functions** (Funzioni DNS).
* Immetti l'**indirizzo IP** per il dominio nel campo **Ip**.
* Immetti il **nome dominio** nel campo **Domain** (Dominio).

**Nota:** in alternativa, è possibile creare un account dominio con la guida [Create an Account](http://docs.cpanel.net/twiki/bin/view/AllDocumentation/WHMDocs/CreateAccount) (Creazione di un account) nella documentazione WHM di cPanel.

## Assegna un IP al server dei nomi

* Seleziona **Nameserver IPs** (IP server dei nomi) dal menu **Network Setup** (Configurazione della rete).
* Immetti il primo **nome di server dei nomi** nel campo **Nameserver** (Server dei nomi).
* Seleziona il pulsante **Assign** (Assegna).
* Ripeti la procedura suindicata per ogni server dei nomi.

## Configura il server dei nomi

* Seleziona **Nameserver Setup** (Configurazione del server dei nomi) dal menu **Service Configuration** (Configurazione del servizio).
* Seleziona il pulsante **Proceed** (Procedi) nel messaggio a comparsa.
