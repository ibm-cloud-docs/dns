---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Select Basic cPanel, Private Nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Creazione di server dei nomi privati in cPanel/WHM
{:#create-private-nameservers-in-cpanel-whm}

Utilizzando il prodotto cPanel/WHM, puoi creare dei server dei nomi privati in qualsiasi momento. I server dei nomi privati consentono ai server dei nomi associati a un sito web (ad esempio `www.yourdomain.com`) di visualizzare il server dei nomi del sito web (ad esempio `ns1.yourdomain.com`) invece del server dei nomi associato all'host web per il sito web (ad esempio `ns1.webhostdomain.com`). L'aggiunta di un server dei nomi privato a un dominio consente anche di accedere a opzioni aggiuntive per la gestione DNS in cPanel/WHM. Attieniti alla procedura in quest'articolo per creare un server dei nomi privato. Se si verificano dei problemi durante o dopo l'esecuzione di questa procedura, [apri un ticket](/docs/get-support?topic=get-support-getting-customer-support).

## Denomina il server dei nomi
{:#name-the-nameserver}

* Accedi a WHM sul tuo server al seguente URL: `http://xx.xx.xx.xx:2086`.
* Seleziona **Basic cPanel/WHM Setup** (Configurazione cPanel/WHM) di base) dal menu **Server Configuration** (Configurazione server).
* Immetti il nome o i nomi host di server dei nomi desiderati in uno o più dei seguenti campi:
  * Primary Nameserver (Server dei nomi primario)
  * Secondary Nameserver (Server dei nomi secondario)
  * Tertiary Nameserver (Server dei nomi terziario)
  * Quaternary Nameserver (Server dei nomi quaternario)
* Seleziona il pulsante **Save** (Salva).

## Crea un file di zona per il dominio
{:#create-a-zone-file-for-the-domain}

* Seleziona **Add a DNS Zone** (Aggiungi una zona DNS) dal menu **DNS Functions** (Funzioni DNS).
* Immetti l'**indirizzo IP** per il dominio nel campo **Ip**.
* Immetti il **nome dominio** nel campo **Domain** (Dominio).

In alternativa, è possibile creare un account dominio con la guida [Create an Account](https://docs.cpanel.net/display/70Docs/Create+a+New+Account) (Creazione di un account) nella documentazione WHM di cPanel.
{:note}

## Assegna un IP al server dei nomi
{:#assign-an-ip-to-the-nameserver}

* Seleziona **Nameserver IPs** (IP server dei nomi) dal menu **Network Setup** (Configurazione della rete).
* Immetti il primo **nome di server dei nomi** nel campo **Nameserver** (Server dei nomi).
* Seleziona il pulsante **Assign** (Assegna).
* Ripeti la procedura suindicata per ogni server dei nomi.

## Configura il server dei nomi
{:#setup-the-nameserver}

* Seleziona **Nameserver Setup** (Configurazione del server dei nomi) dal menu **Service Configuration** (Configurazione del servizio).
* Seleziona il pulsante **Proceed** (Procedi) nel messaggio a comparsa.
