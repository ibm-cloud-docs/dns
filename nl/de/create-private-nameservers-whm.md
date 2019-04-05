---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Select Basic cPanel, Private Nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Private Namensserver in cPanel/WHM erstellen
{:#create-private-nameservers-in-cpanel-whm}

Mit dem Produkt cPanel/WHM können Sie jederzeit private Namensserver erstellen. Private Namensserver ermöglichen den Namensservern, die einer Website zugeordnet sind (z. B. `www.ihredomäne.com`) das Anzeigen der Namensserver der Website (z. B. `ns1.ihredomäne.com`) anstelle des Namensservers, der dem Web-Host für die Website zugeordnet ist (z. B. `ns1.webhostdomäne.com`). Durch das Hinzufügen eines privaten Namensservers zu einer Domäne werden außerdem zusätzliche Optionen für das DNS-Management in cPanel/WHM bereitgestellt. Führen Sie die im vorliegenden Abschnitt beschriebenen Schritte aus, um einen privaten Namensserver zu erstellen. Wenn während oder nach dem Ausführen dieser Prozedur Probleme auftreten, [öffnen Sie ein Ticket](/docs/get-support?topic=get-support-getting-customer-support).

## Namensserver benennen
{:#name-the-nameserver}

* Melden Sie sich auf Ihrem Server unter der folgenden URL bei WHM an: `http://xx.xx.xx.xx:2086`.
* Wählen Sie die Option **cPanel/WHM - Basiskonfiguration** im Menü **Serverkonfiguration** aus.
* Geben Sie den/die gewünschte(n) Hostnamen in mindestens einem der folgenden Felder ein:
  * Primärer Namensserver
  * Sekundärer Namensserver
  * Tertiärer Namensserver
  * Quartärer Namensserver
* Wählen Sie die Schaltfläche **Speichern** aus.

## Zonendaten für die Domäne erstellen
{:#create-a-zone-file-for-the-domain}

* Wählen Sie **DNS-Zone hinzufügen** im Menü **DNS-Funktionen** aus.
* Geben Sie die **IP-Adresse** für die Domäne in das Feld **IP** ein.
* Geben Sie den **Domänennamen** in das Feld **Domäne** ein.

Alternativ kann ein Domänenkonto mit der Anleitung [Konto erstellen](https://docs.cpanel.net/display/70Docs/Create+a+New+Account) der cPanel/WHM-Dokumentation erstellt werden.
{:note}

## IP-Adresse für Namensserver zuordnen
{:#assign-an-ip-to-the-nameserver}

* Wählen Sie **Namensserver-IPs** im Menü **Netzkonfiguration** aus.
* Geben Sie den ersten **Namen des Namensservers** in das Feld **Namensserver** ein.
* Wählen Sie die Schaltfläche **Zuordnen** aus.
* Wiederholen Sie diese Schritte für jeden Namensserver.

## Namensserver einrichten
{:#setup-the-nameserver}

* Wählen Sie **Namensserver konfigurieren** im Menü **Servicekonfiguration** aus.
* Wählen Sie die Schaltfläche **Weiter** in der Popup-Nachricht aus.
