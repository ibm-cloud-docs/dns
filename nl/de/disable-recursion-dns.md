---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Disable Recursion, DNS IBM Cloud DNS servers, BIND configuration file

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Rekursion für DNS inaktivieren
{:#disable-recursion-for-dns}

IBM Cloud DNS-Server führen die Rekursion standardmäßig aus. Mithilfe der Rekursion können Ihre DNS-Server bei Bedarf von anderen DNS-Servern Unterstützung zum Auflösen von Domänennamen anfordern. Die Rekursion kann ein hilfreiches Tool sein, aber sie bietet auch eine Angriffsfläche für Hackerattacken auf den DNS-Server und kann dazu führen, dass der DNS-Server nicht mehr betriebsbereit ist. Generell sollten die Systemadministratoren über den Einsatz der Rekursion entscheiden und entsprechende Aktionen ausführen. Andernfalls sollte die Rekursion inaktiviert bleiben. Führen Sie je nach Betriebssystem oder Systemsteuerung die folgenden Schritte aus, um die DNS-Rekursion zu inaktivieren.

## Rekursion unter Plesk inaktivieren
{:#disable-recursion-in-plesk}
* Melden Sie sich beim **Plesk-Administrations-Panel** an.
* Wählen Sie **Tools und Einstellungen** aus.
* Klicken Sie in dem Abschnitt auf **DNS-Template**.
* Wählen Sie **Localnets** im Abschnitt **DNS-Rekursionseinstellungen** aus.
* Klicken Sie auf die Schaltfläche **OK**.

## Rekursion unter Windows Server 2003 und 2008 inaktivieren
{:#disable-recursion-in-windows-server}

* So rufen Sie den **DNS-Manager** über das Menü **Start** auf:
  * Klicken Sie auf die Schaltfläche **Start**.
  * Wählen Sie **Verwaltung** aus.
  * Wählen Sie **DNS** aus.
* Klicken Sie mit der rechten Maustaste auf den gewünschten **DNS-Server** in der **Konsolenstruktur**.
* Wählen Sie die Registerkarte **Eigenschaften** aus.
* Klicken Sie auf die Schaltfläche **Erweitert** im Abschnitt **Serveroptionen**.
* Wählen Sie das Kontrollkästchen **Rekursionsvorgang deaktivieren** aus.
* Klicken Sie auf die Schaltfläche **OK**.

## Rekursion unter Linux inaktivieren
{:#disable-recursion-in-linux}

 * Lokalisieren Sie die BIND-Konfigurationsdatei im Betriebssystem. Die BIND-Konfigurationsdatei befindet sich in der Regel in einem der folgenden Pfade:
  * /etc/bind/named.conf
  * /etc/named.conf
* Öffnen Sie die Datei named.conf in Ihrem bevorzugten Editor.
* Fügen Sie die folgenden Angaben im Abschnitt **Options** hinzu:<br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* Starten Sie die Einheit erneut.
