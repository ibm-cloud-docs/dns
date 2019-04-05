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

# Sekundäre DNS-Zone löschen
{:#delete-a-secondary-dns-zone}

Eine sekundäre DNS-Zone kann jederzeit gelöscht werden, nachdem sie erstellt wurde. Beachten Sie, dass eine sekundäre DNS-Zone nach dem Löschen nicht wiederhergestellt werden kann. Führen Sie die folgenden Schritte aus, um eine sekundäre DNS-Zone zu löschen.

 * Navigieren Sie zur Anzeige **Sekundäre DNS-Zonen** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/), indem Sie im Navigationsmenü die Option **Klassische Infrastruktur** auswählen. 
* Wählen Sie im Navigationsmenü 'Klassische Infrastruktur' die Optionen **Netz > DNS > Sekundäre Zonen** aus.
* Wählen Sie die Aktion **Löschen** in der Dropdown-Liste **Aktionen** für die Zone aus, die gelöscht werden soll. Ein Bestätigungsfenster wird angezeigt.
  Wenn mehrere sekundäre Zonen vorhanden sind, kann die Ansicht gefiltert werden, um die Zone zu lokalisieren, die gelöscht werden soll.
  {:note}
* Wählen Sie die Schaltfläche **Ja** aus, um das Löschen zu bestätigen, oder wählen Sie die Schaltfläche **Nein** aus, um die Aktion abzubrechen.

## Weitere Schritte
{:#delete-a-secondary-dns-zone-next}

Nachdem eine sekundäre DNS-Zone gelöscht wurde, werden keine weiteren automatischen Übertragungen aus der primären Zone durchgeführt und die sekundäre Zone ist nicht mehr vorhanden. Falls für die primäre Zone später eine sekundäre DNS-Zone benötigt wird, können Sie jederzeit eine neue [sekundäre DNS-Zone erstellen](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone).
