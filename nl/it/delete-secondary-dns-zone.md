---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Eliminazione di una zona DNS secondaria
{:#delete-a-secondary-dns-zone}

Dopo essere stata creata, una zona DNS secondaria può essere eliminata in qualsiasi momento. Tieni presente che, se viene eliminata, una zona DNS secondaria non può essere recuperata. Attieniti alla seguente procedura per eliminare un record DNS secondario.

 * Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Secondary Zones** (Rete - DNS - Zone secondarie) dal menu di navigazione dell'infrastruttura classica.
* Seleziona **Delete** (Elimina) dall'elenco a discesa **Actions** (azioni) per la zona per cui è richiesta l'eliminazione. Verrà visualizzata una casella a comparsa di conferma.
  Se esistono più zone secondarie, è possibile filtrare la vista per individuare la zona da eliminare.
  {:note}
* Seleziona il pulsante **Yes** (Sì) per confermare l'eliminazione oppure seleziona il pulsante **No** per annullare l'azione.

## Cosa succede poi
{:#delete-a-secondary-dns-zone-next}

Dopo che una zona DNS secondaria è stata eliminata, i trasferimenti automatizzati dalla zona primaria cesseranno e la zona secondaria non esisterà più. Se in un qualsiasi momento è necessaria una zona DNS secondaria per la zona primaria, [è possibile creare una zona DNS secondaria](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone) nuovamente.
