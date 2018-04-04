---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Private Namensserver in cPanel/WHM erstellen

Mit dem Produkt cPanel/WHM können Sie jederzeit private Namensserver erstellen. Private Namensserver ermöglichen den Namensservern, die einer Website zugeordnet sind (z. B. `www.ihredomäne.com`) das Anzeigen der Namensserver der Website (z. B. `ns1.ihredomäne.com`) anstelle des Namensservers, der dem Web-Host für die Website zugeordnet ist (z. B. `ns1.webhostdomäne.com`). Durch das Hinzufügen eines privaten Namensservers zu einer Domäne werden außerdem zusätzliche Optionen für das DNS-Management in cPanel/WHM bereitgestellt. Führen Sie die im vorliegenden Abschnitt beschriebenen Schritte aus, um einen privaten Namensserver zu erstellen. Wenn während oder nach dem Ausführen dieser Prozedur Probleme auftreten, [öffnen Sie ein Ticket](/general/create-ticket.html).

## Namensserver benennen

* Melden Sie sich auf Ihrem Server unter der folgenden URL bei WHM an: http://xx.xx.xx.xx:2086.
* Wählen Sie die Option **cPanel/WHM - Basiskonfiguration** im Menü **Serverkonfiguration** aus.
* Geben Sie den/die gewünschte(n) Hostnamen in mindestens einem der folgenden Felder ein:
  * Primärer Namensserver
  * Sekundärer Namensserver
  * Tertiärer Namensserver
  * Quartärer Namensserver
* Wählen Sie die Schaltfläche **Speichern** aus.

## Zonendaten für die Domäne erstellen

* Wählen Sie **DNS-Zone hinzufügen** im Menü **DNS-Funktionen** aus.
* Geben Sie die **IP-Adresse** für die Domäne in das Feld **IP** ein.
* Geben Sie den **Domänennamen** in das Feld **Domäne** ein.

**Hinweis:** Alternativ kann ein Domänenkonto mit der Anleitung [Konto erstellen](http://docs.cpanel.net/twiki/bin/view/AllDocumentation/WHMDocs/CreateAccount) der cPanel/WHM-Dokumentation erstellt werden.

## IP-Adresse für Namensserver zuordnen

* Wählen Sie **Namensserver-IPs** im Menü **Netzkonfiguration** aus.
* Geben Sie den ersten **Namen des Namensservers** in das Feld **Namensserver** ein.
* Wählen Sie die Schaltfläche **Zuordnen** aus.
* Wiederholen Sie diese Schritte für jeden Namensserver.

## Namensserver einrichten

* Wählen Sie **Namensserver konfigurieren** im Menü **Servicekonfiguration** aus.
* Wählen Sie die Schaltfläche **Weiter** in der Popup-Nachricht aus.
