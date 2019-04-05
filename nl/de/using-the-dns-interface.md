---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS-Schnittstelle verwenden
{:#how-to-use-the-dns-interface}

Führen Sie die folgenden Schritte aus, um die DNS-Schnittstelle über das IBM Cloud-Kundenportal zu  verwenden:

* Navigieren Sie zum [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/).
* Wählen Sie im Navigationsmenü die Option **Klassische Infrastruktur** aus.
* Wählen Sie **Netz->DNS->Forward-Zonen** aus.
* Wählen Sie die Domäne aus, die Sie verwalten möchten, oder wählen Sie die Schaltfläche **DNS-Zone hinzufügen** rechts auf der Seite aus.

## DNS-Schnittstelle - Übersicht
{:#dns-interface-overview}
Die DNS-Schnittstelle im Kundenportal bietet Ihnen den vollen Funktionsumfang zum Verwalten aller Aspekte Ihres DNS. Sie können alle Arten von DNS-Managementaktionen in allen Anzeigen der Schnittstelle mit der statischen Menüleiste im oberen Bereich der Anzeige ausführen.

## DNS verwalten
{:#manage-dns}
Beim Öffnen der DNS-Schnittstelle im Portal werden Sie direkt zur Anzeige **DNS verwalten** geleitet, über die Sie alle vorhandenen primären DNS anzeigen, bearbeiten oder löschen können, die Ihrem Konto zugeordnet sind.

* Um neue Datensätze hinzuzufügen, füllen Sie einfach die Felder unter **Neuen Datensatz hinzufügen** aus und klicken Sie auf die Schaltfläche **Datensatz hinzufügen**.
* Um einen vorhandenen Datensatz zu ändern, klicken Sie auf die Zeile, die den Datensatz enthält, um den Modus **Bearbeiten** zu aktivieren. Geben Sie die gewünschten Werte für die Einstellungen an und klicken Sie auf **Aktualisieren**.
* Um einen Datensatz zu löschen, wählen Sie den roten Kreis rechts neben dem Datensatz aus und klicken Sie anschließend in der Eingabeaufforderung auf **Ja**.

## Sekundäres DNS
{:#secondary-dns}

* Navigieren Sie zum [Kundenportal - Klassische Infrastruktur ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/).
* Wählen Sie im Navigationsmenü die Option **Klassische Infrastruktur** aus.
* Wählen Sie **Netz->DNS->Sekundäre Zonen** aus.

In dieser Anzeige können Sie Einstellungen für sekundäre DNS hinzufügen oder ändern.

* Um einen neuen Datensatz hinzuzufügen, wählen Sie **Zone hinzufügen** aus, füllen Sie die Felder aus und wählen Sie anschließend **Hinzufügen** aus.
* Um einen sekundären DNS-Datensatz zu entfernen oder in einen primären Datensatz umzuwandeln, verwenden Sie das Dropdown-Menü **Aktionen** rechts auf der Seite und wählen die gewünschte Option aus.

## Reverse DNS
{:#reverse-dns}

Führen Sie die folgenden Schritte aus, um die DNS-Schnittstelle über die Portalnavigation zu verwenden:

* Navigieren Sie zum [Kundenportal - Klassische Infrastruktur ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/).
* Wählen Sie im Navigationsmenü die Option **Klassische Infrastruktur** aus.
* Wählen Sie **Netz->DNS->Reverse-Datensätze** aus.
* Wählen Sie im Dropdown-Menü die IP-Adresse aus oder geben Sie die IP-Adresse ein, für die Sie das Reverse DNS ändern möchten, und wählen Sie anschließend **IP-Adresse zum Anzeigen** aus.
  * Um den Datensatz hinzuzufügen, geben Sie den Hostnamen ein, den Sie für den Reverse DNS-Eintrag verwenden möchten.
  * Legen Sie die Lebensdauer (TTL, Time to Live) für den Datensatz fest.
  * Wenn die Angaben korrekt sind, wählen Sie **Speichern** aus.

Sie können ein ganzes Teilnetz ändern, indem Sie auf **RDNS für alle IPs in diesem Teilnetz bearbeiten** rechts auf der Seite klicken.

* Wählen Sie auf dieser Seite die Zeile für die IP-Adresse aus, die Sie aktualisieren möchten.
* Geben Sie die entsprechenden Informationen in die Felder ein und wählen Sie anschließend **Aktualisieren** aus. Das Feld "Hinweise" ist optional.

<!--## Propagation Check

* Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network > Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
