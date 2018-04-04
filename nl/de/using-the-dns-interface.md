---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS-Schnittstelle verwenden

Führen Sie die folgenden Schritte aus, um die DNS-Schnittstelle über das IBM Cloud-Kundenportal zu  verwenden:

* Navigieren Sie zum [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/).
* Wählen Sie **Netz->DNS->Forward-Zonen** aus.
* Wählen Sie die Domäne aus, die Sie verwalten möchten, oder wählen Sie die Schaltfläche **DNS-Zone hinzufügen** rechts auf der Seite aus.

## DNS-Schnittstelle - Übersicht
Die DNS-Schnittstelle im Kundenportal bietet Ihnen den vollen Funktionsumfang zum Verwalten aller Aspekte Ihres DNS. Sie können alle Arten von DNS-Managementaktionen in allen Anzeigen der Schnittstelle mit der statischen Menüleiste im oberen Bereich der Anzeige ausführen.

## DNS verwalten
Beim Öffnen der DNS-Schnittstelle im Portal werden Sie direkt zur Anzeige **DNS verwalten** geleitet, über die Sie alle vorhandenen primären DNS anzeigen, bearbeiten oder löschen können, die Ihrem Konto zugeordnet sind.

* Um neue Datensätze hinzuzufügen, füllen Sie einfach die Felder unter **Neuen Datensatz hinzufügen** aus und klicken Sie auf die Schaltfläche **Datensatz hinzufügen**.
* Um einen vorhandenen Datensatz zu ändern, klicken Sie auf die Zeile, die den Datensatz enthält, um den Modus **Bearbeiten** zu aktivieren. Geben Sie die gewünschten Werte für die Einstellungen an und klicken Sie auf **Aktualisieren**.
* Um einen Datensatz zu löschen, wählen Sie den roten Kreis rechts neben dem Datensatz aus und klicken Sie anschließend in der Eingabeaufforderung auf **Ja**.

## Sekundäres DNS

* Navigieren Sie zum [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/).
* Wählen Sie **Netz->DNS->Sekundäre Zonen** aus.

In dieser Anzeige können Sie Einstellungen für sekundäre DNS hinzufügen oder ändern.

* Um einen neuen Datensatz hinzuzufügen, wählen Sie **Zone hinzufügen** aus, füllen Sie die Felder aus und wählen Sie anschließend **Hinzufügen** aus.
* Um einen sekundären DNS-Datensatz zu entfernen oder in einen primären Datensatz umzuwandeln, verwenden Sie das Dropdown-Menü **Aktionen** rechts auf der Seite und wählen die gewünschte Option aus.

## Reverse DNS

Führen Sie die folgenden Schritte aus, um die DNS-Schnittstelle über die Portalnavigation zu verwenden:

* Navigieren Sie zum [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/).
* Wählen Sie **Netz->DNS->Reverse-Datensätze** aus.
* Wählen Sie im Dropdown-Menü die IP-Adresse aus oder geben Sie die IP-Adresse ein, für die Sie das Reverse DNS ändern möchten, und wählen Sie anschließend **IP-Adresse zum Anzeigen** aus.
  * Um den Datensatz hinzuzufügen, geben Sie den Hostnamen ein, den Sie für den Reverse DNS-Eintrag verwenden möchten.
  * Legen Sie die Lebensdauer (TTL, Time to Live) für den Datensatz fest.
  * Wenn die Angaben korrekt sind, wählen Sie **Speichern** aus.

Sie können ein ganzes Teilnetz ändern, indem Sie auf **RDNS für alle IPs in diesem Teilnetz bearbeiten** rechts auf der Seite klicken.

* Wählen Sie auf dieser Seite die Zeile für die IP-Adresse aus, die Sie aktualisieren möchten.
* Geben Sie die entsprechenden Informationen in die Felder ein und wählen Sie anschließend **Aktualisieren** aus. Das Feld "Hinweise" ist optional.

## Weitergabe prüfen

* Navigieren Sie zum [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/).
* Wählen Sie **Netz->Tools** aus.

Auf der Seite, die geöffnet wird, können Sie mehrere Tools auswählen. Verwenden Sie die untere Option, um die Weitergabe Ihres Domänennamens durch die DNS-Server zu prüfen.

* Geben Sie die entsprechenden Informationen in die Felder ein und wählen Sie anschließend **DNS prüfen** aus.
* Nach wenigen Momenten wird das Feld rechts mit den aktuellen DNS-Informationen für die Domäne aktualisiert.
