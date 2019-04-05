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

# Sekundäre DNS-Zone in primäre Zone umwandeln
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

Eine [Sekundäre DNS-Zone](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window} kann jederzeit in eine primäre Zone umgewandelt werden. Beim Umwandeln einer sekundären DNS-Zone in eine primäre DNS-Zone werden die {{site.data.keyword.BluSoftlayer_notm}}-Namensserver zu den maßgeblichen Namensservern für die umgewandelte Zone. Führen Sie die folgenden Schritte aus, um eine sekundäre DNS-Zone in eine primäre DNS-Zone umzuwandeln:

* Navigieren Sie zur Anzeige **Sekundäre DNS-Zonen** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/), indem Sie im Navigationsmenü die Option **Klassische Infrastruktur** auswählen. 
* Wählen Sie im Navigationsmenü 'Klassische Infrastruktur' die Optionen **Netz > DNS > Sekundäre Zonen** aus.
* Wählen Sie **In primäre Zone umwandeln** in der Dropdown-Liste **Aktionen** für die gewünschte sekundäre Zone aus.
* Wählen Sie die Schaltfläche **Ja** aus, damit die Zone umgewandelt wird, oder wählen Sie **Nein** aus, um die Aktion abzubrechen.

## Weitere Schritte
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

Nach dem Umwandeln der sekundären DNS-Zone in eine primäre DNS-Zone wird die umgewandelte Zone in der Anzeige **Forward-Zonen** angezeigt. Alle SOA- und NS-Datensätze, die vorher für die Zone vorhanden waren, werden durch {{site.data.keyword.BluSoftlayer_notm}}-SOA- und -NS-Datensätze ersetzt, die nicht bearbeitet werden können. Sie können die [übrigen Zonendatensätze weiterhin bearbeiten](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record).
