---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Eliminazione di una zona DNS secondaria

Dopo essere stata creata, una zona DNS secondaria può essere eliminata in qualsiasi momento. Tieni presente che, se viene eliminata, una zona DNS secondaria non può essere recuperata. Attieniti alla seguente procedura per eliminare un record DNS secondario.

 * Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/). Fai riferimento a [Using the DNS Zones Screen](use-dns-zones-screen.html){:new_window} (Utilizzo della schermata DNS Zones (Zone DNS)).
* Seleziona **Delete** (Elimina) dall'elenco a discesa **Actions** (azioni) per la zona per cui è richiesta l'eliminazione. Verrà visualizzata una casella a comparsa di conferma.
  **Nota:** se esistono più zone secondarie, la vista può essere filtrata per individuare la zona da eliminare.
* Seleziona il pulsante **Yes** (Sì) per confermare l'eliminazione oppure seleziona il pulsante **No** per annullare l'azione.

## Cosa succede poi

Dopo che una zona DNS secondaria è stata eliminata, i trasferimenti automatizzati dalla zona primaria cesseranno e la zona secondaria non esisterà più. Se in un qualsiasi momento è necessaria una zona DNS secondaria per la zona primaria, [è possibile creare una zona DNS secondaria](add-secondary-dns-zone.html) nuovamente.
