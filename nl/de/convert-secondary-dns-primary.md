---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Sekundäre DNS-Zone in primäre Zone umwandeln

Eine [Sekundäre DNS-Zone](add-secondary-dns-zone.html){:new_window} kann jederzeit in eine primäre Zone umgewandelt werden. Beim Umwandeln einer sekundären DNS-Zone in eine primäre DNS-Zone werden die {{site.data.keyword.BluSoftlayer_notm}}-Namensserver zu den maßgeblichen Namensservern für die umgewandelte Zone. Führen Sie die folgenden Schritte aus, um eine sekundäre DNS-Zone in eine primäre DNS-Zone umzuwandeln:

* Navigieren Sie zur Anzeige **Sekundäre DNS-Zonen** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/). Weitere Informationen finden Sie unter [Anzeige 'DNS-Zonen' verwenden](use-dns-zones-screen.html){:new_window}.
* Wählen Sie **In primäre Zone umwandeln** in der Dropdown-Liste **Aktionen** für die gewünschte sekundäre Zone aus.
* Wählen Sie die Schaltfläche **Ja** aus, damit die Zone umgewandelt wird, oder wählen Sie **Nein** aus, um die Aktion abzubrechen.

## Weitere Schritte

Nach dem Umwandeln der sekundären DNS-Zone in eine primäre DNS-Zone wird die umgewandelte Zone in der Anzeige **Forward-Zonen** angezeigt. Alle SOA- und NS-Datensätze, die vorher für die Zone vorhanden waren, werden durch {{site.data.keyword.BluSoftlayer_notm}}-SOA- und -NS-Datensätze ersetzt, die nicht bearbeitet werden können. Sie können die [übrigen Zonendatensätze weiterhin bearbeiten](edit-dns-zone-record.html).
