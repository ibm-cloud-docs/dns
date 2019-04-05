---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, IBM Cloud, Add Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Sekundäre DNS-Zone hinzufügen
{:#add-a-secondary-dns-zone}

{{site.data.keyword.BluSoftlayer_notm}} stellt sekundäre DNS für alle Kunden bereit, um primäre DNS-Zonen zum Schutz vor Datenverlust zwischenzuspeichern. Das Verwalten einer sekundären DNS-Zone ist nicht obligatorisch. Für Benutzer mit mehreren Domänen wird eine sekundäre DNS-Zone jedoch dringend empfohlen. Führen Sie die folgenden Schritte aus, um eine sekundäre DNS-Zone hinzuzufügen:

* Navigieren Sie zur Anzeige **Sekundäre DNS-Zonen** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/), indem Sie im Navigationsmenü die Option **Klassische Infrastruktur** auswählen. 
* Wählen Sie im Navigationsmenü 'Klassische Infrastruktur' die Optionen **Netz > DNS > Sekundäre Zonen** aus.
* Wählen Sie die Registerkarte **Zone hinzufügen** aus.
* Geben Sie die **Domäne für die Zone** in das Feld **Zone** ein.
* Geben Sie die **IP-Adresse des Master-Namensservers** in das Feld **Master-Namensserver** ein.
* Geben Sie die **Übertragungszeit** (in Minuten), in der die primäre DNS-Zone in die sekundäre DNS-Zone übertragen wird, in das Feld **Übertragungsintervall** ein.
* Wählen Sie die Schaltfläche **Hinzufügen** aus, um die Zone hinzuzufügen, oder wählen Sie **Abbrechen** aus, um die Aktion abzubrechen.

## Weitere Schritte
{:#add-a-secondary-dns-zone-next}

Nach der Erstellung wird die sekundäre DNS-Zone in der Liste der Zonen in der Anzeige 'Sekundäre DNS-Zonen' angezeigt. Die Datenübertragung aus der primären in die sekundäre Zone erfolgt in den Zeitintervallen, die Sie beim Erstellen der Zone angeben. Sie können die Zone jederzeit [bearbeiten](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record), [manuell übertragen](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) oder in eine primäre Zone [umwandeln](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone). Außerdem kann die sekundäre DNS-Zone jederzeit [gelöscht](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone) werden.
