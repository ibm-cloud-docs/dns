---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Sekundäre DNS-Zone hinzufügen

{{site.data.keyword.BluSoftlayer_notm}} stellt sekundäre DNS für alle Kunden bereit, um primäre DNS-Zonen zum Schutz vor Datenverlust zwischenzuspeichern. Das Verwalten einer sekundären DNS-Zone ist nicht obligatorisch. Für Benutzer mit mehreren Domänen wird eine sekundäre DNS-Zone jedoch dringend empfohlen. Führen Sie die folgenden Schritte aus, um eine sekundäre DNS-Zone hinzuzufügen:

* Navigieren Sie zur Anzeige **Sekundäre DNS-Zonen** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/). Weitere Informationen finden Sie unter [Anzeige 'DNS-Zonen' verwenden](use-dns-zones-screen.html){:new_window}.
* Wählen Sie die Registerkarte **Zone hinzufügen** aus.
* Geben Sie die **Domäne für die Zone** in das Feld **Zone** ein.
* Geben Sie die **IP-Adresse des Master-Namensservers** in das Feld **Master-Namensserver** ein.
* Geben Sie die **Übertragungszeit** (in Minuten), in der die primäre DNS-Zone in die sekundäre DNS-Zone übertragen wird, in das Feld **Übertragungsintervall** ein.
* Wählen Sie die Schaltfläche **Hinzufügen** aus, um die Zone hinzuzufügen, oder wählen Sie **Abbrechen** aus, um die Aktion abzubrechen.

## Weitere Schritte

Nach der Erstellung wird die sekundäre DNS-Zone in der Liste der Zonen in der Anzeige 'Sekundäre DNS-Zonen' angezeigt. Die Datenübertragung aus der primären in die sekundäre Zone erfolgt in den Zeitintervallen, die Sie beim Erstellen der Zone angeben. Sie können die Zone jederzeit [bearbeiten](edit-secondary-dns-zone.html), [manuell übertragen](make-manual-zone-transfer-secondary-dns.html) oder in eine primäre Zone [umwandeln](convert-secondary-dns-zone-primary-zone.html). Außerdem kann die sekundäre DNS-Zone jederzeit [gelöscht](delete-secondary-dns-zone.html) werden.
