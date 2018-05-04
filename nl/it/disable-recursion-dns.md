---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Disabilitazione della ricorsione per DNS

I server DNS di IBM Cloud eseguono la ricorsione per impostazione predefinita. La ricorsione consente al tuo server DNS di contattare altri server DNS per un ausilio nella risoluzione dei nomi dominio quando non riesce esso stesso a risolvere il dominio. La ricorsione si può rivelare uno strumento utile, quando è necessario; tuttavia, espone anche il server DNS ad attacchi che potrebbero addirittura causarne l'arresto. Gli amministratori di sistema in genere identificano quando è necessaria la ricorsione e agiscono di conseguenza. Altrimenti, è meglio disabilitare la ricorsione. Attieniti alla seguente procedura basata sul tuo sistema operativo o sul pannello di controllo per disabilitare la ricorsione DNS.

## Disabilita la ricorsione in Plesk
* Accedi al **Plesk Admin Panel** (Pannello di amministrazione Plesk).
* Seleziona **Tools and Settings** (Strumenti e impostazioni).
* Fai clic su **DNS Template Settings** (Impostazioni modello DNS) dalla sezione.
* Seleziona **Localnets** (Reti locali) dalla sezione **DNS Recursion** (Ricorsione DNS).
* Fai clic sul pulsante **OK**.

## Disabilita la ricorsione in Windows Server 2003 e 2008

* Usa il **Gestore DNS** dal menu **Start**:
  * Fai clic sul pulsante **Start**.
  * Seleziona **Strumenti di amministrazione**.
  * Seleziona **DNS**.
* Fai clic con il pulsante destro del mouse sul **Server DNS** desiderato nell'**Albero console**.
* Seleziona la scheda **Proprietà**.
* Fai clic sul pulsante **Avanzate** nella sezione **Opzioni server**.
* Seleziona la casella di spunta **Disattiva query ricorsiva**.
* Fai clic sul pulsante **OK**.

## Disabilita la ricorsione in Linux

 * Individua il file di configurazione BIND nel sistema operativo. Il file di configurazione BIND di norma si trova in uno dei seguenti percorsi:
  * /etc/bind/named.conf
  * /etc/named.conf
* Apri il file named.conf nel tuo editor preferito.
* Aggiungi i seguenti dettagli alla sezione **Options**:<br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* Riavvia il dispositivo.
