---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-04-10"

keywords: DNS servers, fast domain name resolution, DNS FAQ

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}


# Domande frequenti di DNS
{:#dns-faq}

## Quali sono i server DNS?
{:#what-are-dns-servers}
{: faq}

161.26.0.10 e 161.26.0.11

## Quali sono i resolver DNS locali?
{:#what-are-local-dns-resolvers}
{: faq}

I server dei nomi di risoluzione locali sulla nostra rete privata sono:

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Questi server dei nomi forniscono una rapida risoluzione dei nomi dominio che non usa la tua allocazione di larghezza di banda pubblica. Per usarli, attieniti alla corretta procedura per aggiungere dei server dei nomi di risoluzione al tuo sistema operativo.

## Quali sono gli indirizzi dei server dei nomi {{site.data.keyword.BluSoftlayer_notm}}?
{:#what-are-name-server-addresses}
{: faq}

Abbiamo due indirizzi per i server dei nomi autorevoli e due indirizzi per i server dei nomi di risoluzione.

### Server dei nomi autorevoli
{:#authoratative-name-servers}

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### Server dei nomi di risoluzione
{:#resolving-name-servers}

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Questi server dei nomi di risoluzione si trovano sulla nostra rete privata e, pertanto, non usano la tua allocazione di larghezza di banda pubblica. 

## Quali server DNS di IBM Cloud risponderanno per i miei domini secondari?
{:#what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}

I server DNS autorevoli {{site.data.keyword.BluSoftlayer_notm}} Anycast abilitati a IPv risponderanno per i tuoi domini secondari. Questi server si trovano ai seguenti indirizzi:

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## Quali indirizzi IP verranno utilizzati per i miei trasferimenti di zona di domini secondari?
{:#which-ipaddresses-secondary-domain-zone-transfers}
{: faq}

I trasferimenti per i tuoi domini secondari proverranno da uno dei seguenti quattro indirizzi IP:

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## Qual è la differenza tra i server dei nomi pubblici e privati?
{:#public-v-private-nameservers}
{: faq}

I nostri server dei nomi pubblici fungono da server dei nomi autorevoli per i nomi dominio che si trovano nei nostri server DNS e sono gestiti tramite il [Portale cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). Questi server "rispondono" e "risolvono" i nomi dominio al tuo indirizzo IP per l'utenza generica di Internet.

I nostri server dei nomi di risoluzione si trovano nella rete privata e fungono da resolver DNS per il tuo server. I resolver privati interrogano i server dei nomi root di Internet per le ricerche di dominio. Ad esempio, l'invio di una email dal tuo server richiede una ricerca del server del nomi (NSlookup) del nome dominio di destinazione. I server DNS privati risolvono queste informazioni sulla rete privata per contenere l'utilizzo della larghezza di banda, ridurre il carico sui server autorevoli e offrire una rapida risoluzione. I resolver di rete privata offrono un servizio di comodità ai nostri clienti.

## Quali sono le mie opzioni di server dei nomi?
{:#what-are-my-name-server-options-faq}
{: faq}

Con un Bare Metal Server, ci sono quattro tipiche opzioni per i server dei nomi:

* Utilizza i server dei nomi del registrar dei nomi dominio per gestire i tuoi nomi dominio.
* Utilizza i server dei nomi {{site.data.keyword.BluSoftlayer_notm}} per gestire i tuoi nomi dominio.
* Utilizza un servizio DNS di terze parti per gestire i tuoi nomi dominio.
* Esegui i tuoi server dei nomi sul tuo server per gestire i tuoi nomi dominio.

Per le prime tre opzioni, utilizzerai i server dei nomi della terza parte (ad esempio `ns1.softlayer.com` e `ns2.softlayer.com`). L'ultima opzione utilizza il tuo dominio come server dei nomi (ad esempio `ns1.yourdomain.com` e `ns2.yourdomain.com`) e richiede che tu esegua i servizi DNS sul tuo server. Devi anche registrare il tuo dominio come un server dei nomi presso il tuo registrar. La registrazione del server dei nomi è di solito gratuita ma richiede un'operazione aggiuntiva oltre al processo di base di registrazione del nome dominio.

I nostri clienti dispongono di servizi DNS gratuiti completamente gestiti tramite il [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/). Ti consigliamo vivamente di affidare a noi di {{site.data.keyword.BluSoftlayer_notm}} la gestione del tuo DNS e dei tuoi server dei nomi poiché abbiamo dei sistemi ridondanti, offriamo facilità d'uso e consentiamo di risolvere rapidamente i problemi correlati a DNS.

## Come configuro il mio DNS inverso?
{:#how-do-i-setup-reverse-dns}
{: faq}

La configurazione di DNS inverso si esegue utilizzando il nostro [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/)  Per le istruzioni su come configurare il tuo DNS inverso, consulta [Aggiornamento di un record di DNS inverso](/docs/infrastructure/dns?topic=dns-update-reverse-dns-record).


## Quanto tempo occorre perché vengano propagate le modifiche di DNS?
{:#how-long-for-dns-changes-propagate}
{: faq}

I tempi di propagazione delle modifiche di DNS dipendono dall'impostazione TTL (Time-to-live) per il record di DNS.

Il TTL predefinito è un giorno, il che significa che la propagazione in tutta Internet delle eventuali modifiche a un nome dominio impiega un giorno. Il TTL può essere ridotto se intendi apportare modifiche frequentemente; tuttavia, più è basso il TTL e più aumenta il carico sul server dei nomi. Dei carichi più elevati possono aumentare il tempo di risposta per gli utenti finali, il che potrebbe avere delle ripercussioni sulla loro soddisfazione complessiva.

Più alto è il valore dell'impostazione del TTL e più elevate saranno le prestazioni di DNS grazie alla memorizzazione in cache dell'ISP locale. Più basso è il valore dell'impostazione del TTL e più ridotte saranno le prestazioni di DNS a causa dell'aumentata risoluzione dei nomi.

Per verificare il TTL, controlla il record SOA (Start of Authority) per il dominio. Un ottimo strumento per riesaminare le informazioni sui domini è offerto da [CentralOps.net ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://centralops.net/co/)

Il TTL è elencato in secondi. Dividi per 60 per convertire il TTL in minuti oppure per 3600 per convertire in ore.


## Dopo il trasferimento di un dominio, quanto tempo ci vuole perché il dominio e le modifiche apportate diventino visibili?
{:#how-long-transfer-change-visiblity}
{: faq}

Il tuo dominio e/o le modifiche a esso apportate sono visibili sui server DNS di IBM Cloud immediatamente dopo il completamento del trasferimento. A causa della natura della propagazione di DNS, ci sarà un ritardo prima che le modifiche siano visibili su altri server DNS.

## Posso completare richieste AXFR sulla rete privata?
{:#axfr-request-private-network}
{: faq}

Attualmente, {{site.data.keyword.BluSoftlayer_notm}} non supporta le richieste AXFR sulla rete privata. Tutte le richieste AXFR devono essere completate sulla rete pubblica.
