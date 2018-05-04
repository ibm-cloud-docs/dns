---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Creazione dei tuoi server dei nomi in Cpanel/WHM

Quest'articolo descrive la procedura per creare i tuoi server dei nomi utilizzando WHM (Web Host Manager). Se hai problemi ad attenerti a questa procedura, invia un ticket di supporto facendo riferimento a quest'articolo.

1. Decidi innanzitutto quali saranno i nomi dei tuoi server dei nomi. Diciamo, ad esempio, che la mia azienda di hosting è denominata “Awesome Server Hosting” e che quindi mi piacerebbe configurare `ns1.awesomeserverhosting.com` e `ns2.awesomeserverhosting.com`.

* Accedi a WHM sul tuo server andando a https://XX.XX.XX.XX:2087 nel tuo browser.

* Per configurare i tuoi server dei nomi, seleziona la prima opzione nella barra a sinistra, che dovrebbe essere “Basic cPanel/WHM Setup” (Configurazione cPanel/WHM di base). 

 * Qui puoi impostare il nome dei server dei nomi primario, secondario, terziario e quaternario.

 * Quando hai finito, seleziona il pulsante “Save” (Salva).

2. Crea ora il file di zona per “awesomeserverhosting.com” nel tuo server. Quest'attività può essere eseguita in due modi:

Primo metodo: crea l'account dominio per “awesomeserverhosting.com”. Le istruzioni per tale operazioni non rientrano nel campo di applicazione del presente articolo; consulta la [documentazione di cPanel](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html) per ulteriori informazioni: 

   * Seleziona “Add a DNS Zone” (Aggiungi una zona DNS) sotto “DNS Functions” (Funzioni DNS) nella barra laterale sinistra.

   * Fornisci gli indirizzi IP dove è ospitato il sito web principale per “awesomeserverhosting.com” e, ovviamente, il nome dominio.

   **Nota: esegui questa operazione solo se non programmi di ospitare `awesomeserverhosting.com` su questo server!**

   * Sotto l'intestazione **Networking Setup** (Configurazione della rete), fai clic su **Nameserver IPs** (IP server dei nomi).

   * Fornisci i nomi dei tuoi server dei nomi. Fornisci ad esempio `ns1.awesomeserverhosting.com` e quindi `ns2.awesomeserverhosting.com`.

   * Nella barra di sinistra, individua **Nameserver Setup** (Configurazione server dei nomi) sotto **Service Configuration** (Configurazione servizio).

   * Verrà visualizzato un messaggio simile al seguente: “We recommend you do not enable the nameserver unless you are going to use it. If you wish to disable the nameserver you can always turn it off in the Service Manager” (Si sconsiglia di abilitare il server dei nomi a meno che non si intenda utilizzarlo. Se si desidera disabilitare il server dei nomi, è sempre possibile disattivarlo nel Service Manager).

   * Il nostro obiettivo e rendere attivi e operativi i nostri server dei nomi; seleziona quindi il pulsante **Proceed >>** (Procedi >>). Lo strumento `cPanel` verificherà che sul tuo server siano installati i pacchetti corretti e che siano configurati per funzionare correttamente per ospitare i tuoi servizi dei nomi. Ora è tutto pronto!

Link esterni:

* [Documentazione di cPanel](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
