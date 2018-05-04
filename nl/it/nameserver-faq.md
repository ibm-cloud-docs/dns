---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Domande frequenti sui server di nomi

## Quali sono gli indirizzi dei server dei nomi IBM Cloud?

Abbiamo due indirizzi per i server dei nomi autorevoli e due indirizzi per i server dei nomi di risoluzione.

**Server dei nomi autorevoli**

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

**Server dei nomi di risoluzione**

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

<a name="27"></a>
## Qual è la differenza tra i server dei nomi pubblici e privati in SoftLayer?

I server dei nomi pubblici fungono da server dei nomi autorevoli per i nomi dominio che si trovano nei nostri server DNS e sono gestiti tramite il Portale del cliente. Questi server "rispondono" e "risolvono" i nomi dominio al tuo indirizzo IP per l'utenza generica di Internet.

I server dei nomi di risoluzione si trovano nella rete privata e fungono da resolver DNS per il tuo server. I resolver privati interrogano i server dei nomi root di Internet per le ricerche di dominio. Ad esempio, l'invio di una email dal tuo server richiede una ricerca del server del nomi (NSlookup) del nome dominio di destinazione. I server DNS privati risolvono queste informazioni sulla rete privata per contenere l'utilizzo della larghezza di banda, ridurre il carico sui server autorevoli e offrire una rapida risoluzione. I resolver di rete privata offrono un servizio di comodità ai nostri clienti.

<a name="28"></a>
## Quali sono le mie opzioni di server dei nomi?

Con un server Bare Metal, ci sono quattro tipiche opzioni per i server dei nomi:

1. Utilizza i server dei nomi del registrar dei nomi dominio per gestire i tuoi nomi dominio.
2. Utilizza i server dei nomi IBM Cloud per gestire i tuoi nomi dominio.
3. Utilizza un servizio DNS di terze parti per gestire i tuoi nomi dominio.
4. Esegui i tuoi server dei nomi sul tuo server per gestire i tuoi nomi dominio.

Per le opzioni 1, 2, e 3, utilizzerai i server dei nomi della terza parte (ad esempio `ns1.softlayer.com` e `ns2.softlayer.com`). Per l'opzione numero 4, utilizzerai il tuo dominio come server dei nomi (`ns1.yourdomain.com` e `ns2.yourdomain.com`). L'opzione numero 4 richiede che tu esegua i servizi DNS sul tuo server e anche che tu esegua la registrazione del tuo dominio come un server dei nomi presso il tuo registrar. Questa registrazione è di solito gratuita ma richiede un'operazione aggiuntiva oltre al processo di base di registrazione del nome dominio.

IBM Cloud offre servizi DNS gratuiti completamente gestiti tramite il [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Ti consigliamo vivamente di affidare a noi di IBM Cloud la gestione del tuo DNS e la funzione come tuoi server dei nomi poiché abbiamo dei sistemi ridondanti, offriamo facilità d'uso e consentiamo di risolvere rapidamente i problemi correlati a DNS.


# Come possono eseguire dei miei server dei nomi?

Il modo più facile per eseguire e gestire i tuoi server dei nomi consiste nell'utilizzare uno strumento di pannello di controllo come **Plesk** o **cPanel**. Entrambi questi prodotti hanno dei server dei nomi dominio integrati che ti consentono di aggiungere, modificare o eliminare nomi dominio.

Per iniziare, registra il tuo nome dominio come un server dei nomi presso il tuo registrar di nome dominio e assegna due indirizzi IP dai tuoi intervalli IP di server.
