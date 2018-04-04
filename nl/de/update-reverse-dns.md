---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Reverse DNS-Datensatz aktualisieren

Mit Reverse DNS können Benutzer die Domäne identifizieren, die einer IP-Adresse zugeordnet ist. Kunden können Ihre Reverse DNS-Datensätze jederzeit aktualisieren, um PTR (Pointer) und TTL (Time to Live) zu ändern. Im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) der **verwalteten** Version können Sie mit dem Tool **Suchen und ersetzen** mehrere PTR-Datensätze gleichzeitig aktualisieren. Mit diesem Tool können Sie einen PTR-Datensatz ganz oder teilweise in das Feld 'Suchen' eingeben und jedes Vorkommen dieser Zeichenfolge in den betreffenden PTR-Datensätzen durch die gewünschte Angabe ersetzen. 

Dabei ist zu beachten, dass dieses Tool nur funktioniert, wenn die vorhandenen PTR-Datensätze dem Server oder dem VLAN zugeordnet sind. Wenn keine PTR-Datensätze vorhanden sind, werden keine Details aufgelistet und Aktualisierungsversuche lösen einen Fehler aus. 

Informationen zum Hinzufügen eines PTR-Datensatzes für Reverse DNS finden Sie unter [Zeigerdatensatz (PTR) hinzufügen oder bearbeiten](add-and-edit-ptr-pointer-record.html). Führen Sie die folgenden Schritte aus, um einen Reverse DNS-Datensatz zu aktualisieren:

 * Navigieren Sie unter Verwendung Ihrer eindeutigen Berechtigungsnachweise zum [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/).
 * Wählen Sie **DNS** im Dropdown-Menü **Netz** aus.
 * Wählen Sie die Menüoption **Reverse DNS** aus.
 * Geben Sie an, ob die Aktualisierung für alle entsprechenden IP-Adressen im VLAN-Netz durchgeführt werden soll oder für eine einzelne IP-Adresse.<br><br><table border="1"><tbody><tr><th>Aktualisierung für...</th><th>Vorgehensweise</th></tr><tr><td>einzelne IP-Adresse</td><td><ul><li>Wählen Sie das <b>Dropdown-Menü</b> aus, um die IP-Adressen anzuzeigen.</li><li>Klicken Sie auf die gewünschte <strong>IP-Adresse</strong>, um die zugeordneten Reverse DNS-Details für den Server anzuzeigen.</li></ul></td></tr><tr><td>alle entsprechenden IP-Adressen in einem VLAN-Netz</td><td><ul><li>Wählen Sie die Option <strong>IP-Adresse zum Anzeigen</strong> aus, nachdem Sie wie oben angegeben eine IP-Adresse ausgewählt haben.</li><li>Wählen Sie die Option <strong>RDNS für alle IPs in diesem Teilnetz bearbeiten</strong> aus.</li></ul></td></tr></tbody></table><br/>
 * Fügen Sie für einzelne IP-Adressen nur **Hostname** und **Reverse-TTL** hinzu und wählen Sie anschließend **Speichern** aus. Markieren Sie für das gesamte **Teilnetz** den freien Bereich unter der Spalte **Reverse DNS**, fügen Sie **Hostname** hinzu und wählen Sie anschließend die Schaltfläche **Aktualisieren** aus. Diese Task muss für jede IP-Adresse in dem Teilnetz ausgeführt werden.
