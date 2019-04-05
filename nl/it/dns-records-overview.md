---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: domain names, Resource Records, host name

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Panoramica di DNS - record risorsa
{:#dns-0verview-resource-records}

## Sezione Record `A`
{:#the-a-record-section}

La maggior parte dei record sarà di tipo **A**. Ciò offre la massima versatilità di puntamento dei tuoi nomi dominio alla destinazione da te desiderata. Ogni record si articola in un nome host e un indirizzo IP.

**Campo Host:** il nome host per quello specifico record A. Il nome host dovrebbe essere quanto precede _.domain.com_ nel tuo nome dominio completo (o FQDN, fully qualified domain name). Ad esempio, su `www.domain.com`, "www" è l'host (senza le virgolette). Indipendentemente da quanto qui elencato, la ricerca accoderà automaticamente “.domain.com” alla query. Un "A record" (Record A) ( _domain.com_ invece di _host.domain.com_) vuoto viene creato inserendo un simbolo '@' nel campo del nome host.

I record "A" comuni includono: `www.domain.com`, `ftp.domain.com`, `mail.domain.com`, `webmail.domain.com`, `mysql.domain.com`

**Campo Points to (Punta a):** questo campo è dove elenchi l'indirizzo IP a cui deve puntare il nome host.

## Sezione `CNAME`
{:#the-cname-section}

I record CNAME puntano ai nomi dominio invece che agli indirizzi IP. Il vantaggio derivante dall'utilizzo di un record CNAME è che consente di puntare un host a uno specifico nome dominio e di modificare quindi solo i record A del nome dominio di destinazione perché la modifica venga effettuata su entrambi i domini. Questo metodo viene di norma utilizzato da chi gestisce più domini di livello superiore (TLD) in diverse versioni (.com, .net, .org, ecc.) dello stesso dominio.

Ad esempio, hai `_domain.com_` e hai anche `_domain.net_` e vuoi che i record puntino allo stesso IP. Puoi creare dei record CNAME per l'host _www_ di `_domain.net_` che puntano a `www.domain.com`. Quindi, per modificare l'host _www_ di `_domain.net_`, non devi fare altro che modificare il record A di `www.domain.com` in modo che punti al suo nuovo indirizzo IP; viene automaticamente modificato anche `www.domain.net`.

Un comune errore derivante dall'utilizzo di questo metodo è che potresti accidentalmente modificare i record per diversi domini quando invece intendevi modificarne solo uno. Vale a dire che ti _devi_ annotare quali domini puntano a quali domini.

**Campo Host:** il nome host per quello specifico record CNAME. Il nome host dovrebbe essere quanto precede .domain.com nel tuo nome dominio completo (o FQDN, fully qualified domain name). Ad esempio, su `www.domain.com`, “www” è l'host (senza le virgolette). Indipendentemente da quanto qui elencato, la ricerca accoderà automaticamente “`.domain.com`” alla query. Un "record A" vuoto (`_domain.com_` anziché `_host.domain.com_`) viene creato inserendo un simbolo `@` nel campo del nome host.

**Campo Points to (Punta a):** il nome a cui punta il record. _Questo campo deve essere un nome dominio, non un indirizzo IP._ Il nome dominio deve anche terminare con un punto. Altrimenti, quando interrogato, il record dominio continuerà fino a trovare il punto successivo nel file di zona.

## Sezione `MX`
{:#the-mx-section}

La sezione MX è l'area che gestisce la direzione della posta.

**Campo Priority (Priorità):** questa sezione ti consente di selezionare la tua preferenza per un singolo record MX. I record vengono elaborati in ordine, iniziando con la priorità più bassa e proseguendo con le priorità più alte. Pertanto, se hai due server di posta oppure un server di posta e uno spooler di posta, imposta la priorità più bassa per il tuo server di posta principale e imposta una priorità più alta per il tuo server di posta di backup o per il tuo spooler di posta.

**Campo Host:** puoi specificare un nome host di posta qui ma, nella maggior parte dei casi, non è necessario. Ti consigliamo di creare un host vuoto (usa un simbolo `@` per il nome host) e di puntarlo al tuo server di posta.

**Campo Goes to (Destinazione):** l'indirizzo del server di posta. Quello che si fa comunemente qui è utilizzare il nome host di posta da te creato nella sezione del record A per puntare alla tua posta.

Si consiglia vivamente di puntare i record MX a un nome dominio che, proprio come un record CNAME, deve terminare con un punto.

## Sezione `TXT`
{:#the-txt-section}

Un record TXT in genere è un record che puoi interrogare e che restituisce informazioni su un dominio. Tali record possono essere utilizzati per gli indicatori SPF, per creare connessioni di porta e protocollo oppure semplicemente per restituire informazioni su un dominio. Sono il più delle volte utilizzati con il protocollo SPF.

**Name (Nome):** l'host da cui può essere interrogato il record TXT.

**Value (Valore):** quanto restituito dal record TXT, tra virgolette.
