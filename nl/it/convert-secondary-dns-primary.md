---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Conversione di una zona DNS secondaria in una zona primaria
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

In qualsiasi momento, è possibile convertire una [zona DNS secondaria](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window} nella tua nuova zona primaria. Quando converti una zona DNS secondaria in primaria, i server dei nomi {{site.data.keyword.BluSoftlayer_notm}} diventano server dei nomi autorevoli per la zona convertita. Attieniti alla procedura di seguito per convertire una zona DNS secondaria in primaria:

* Vai alla schermata **Secondary DNS Zones** (Zone DNS secondarie) nel [Portale del cliente ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/) selezionando **Classic Infrastructure** (Infrastruttura classica) dal menu di navigazione. 
* Seleziona **Network > DNS > Secondary Zones** (Rete - DNS - Zone secondarie) dal menu di navigazione dell'infrastruttura classica.
* Seleziona **Convert to Primary** (Converti in primaria) dall'elenco a discesa **Actions** (Azioni) per la zona secondaria desiderata.
* Seleziona il pulsante **Yes** (Sì) per convertire la zona oppure seleziona **No** per annullare l'azione.

## Cosa succede poi
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

Dopo che hai convertito la zona DNS secondaria in primaria, puoi visualizzarla nella schermata **Forward Zones** (Zone di inoltro). Tutti i record SOA e NS che esistevano in precedenza per la zona verranno sostituiti da record SOA ed NS {{site.data.keyword.BluSoftlayer_notm}}, che non possono essere modificati. Puoi però ancora [modificare i restanti record di zona](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record).
