---
copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-02-26"

keywords: Reverse DNS Record, Reverse DNS, IP address, Individual IP Select

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Reverse DNS-Datensatz aktualisieren
{:#update-reverse-dns-record}

Mit Reverse DNS können Benutzer die Domäne identifizieren, die einer IP-Adresse zugeordnet ist. Kunden können Ihre Reverse DNS-Datensätze jederzeit aktualisieren, um PTR (Pointer) und TTL (Time to Live) zu ändern. In der [IBM Cloud-Konsole ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/) der **verwalteten** Version können Sie mit dem Tool **Suchen und ersetzen** mehrere PTR-Datensätze gleichzeitig aktualisieren. Mit diesem Tool können Sie einen PTR-Datensatz ganz oder teilweise in das Feld 'Suchen' eingeben und jedes Vorkommen dieser Zeichenfolge in den betreffenden PTR-Datensätzen durch die gewünschte Angabe ersetzen. 

Dabei ist zu beachten, dass dieses Tool nur funktioniert, wenn die vorhandenen PTR-Datensätze dem Server oder dem VLAN zugeordnet sind. Wenn keine PTR-Datensätze vorhanden sind, werden keine Details aufgelistet und Aktualisierungsversuche lösen einen Fehler aus. 

Informationen zum Hinzufügen eines PTR-Datensatzes für Reverse DNS finden Sie unter [Zeigerdatensatz (PTR) hinzufügen oder bearbeiten](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record). Führen Sie die folgenden Schritte aus, um einen Reverse DNS-Datensatz zu aktualisieren:

 * Navigieren Sie unter Verwendung Ihrer eindeutigen Berechtigungsnachweise zur [IBM Cloud-Konsole ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/).
 * Wählen Sie im Navigationsmenü die Option **Klassische Infrastruktur** aus.
 * Wählen Sie im Navigationsmenü 'Klassische Infrastruktur' die Optionen **Netz > DNS > Reverse DNS** aus.
 * Geben Sie die IP-Adresse ein oder wählen Sie sie im Dropdown-Menü aus und klicken Sie auf **IP-Adresse zum Anzeigen**.
 * Bearbeiten Sie die aufgeführten Optionen und klicken Sie auf **Speichern**. Sie können auch die Option **RDNS für alle IPs in diesem Teilnetz bearbeiten** auswählen, um Änderungen im gesamten Teilnetz vorzunehmen. 
 

