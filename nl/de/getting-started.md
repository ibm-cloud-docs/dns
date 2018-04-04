---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Einführung in DNS

Das Domain Name System (DNS) im Internet ist eine Methode zum Übersetzen von IP-Adressen, die von Servern und Routern erkannt werden, in benutzerfreundliche konkrete Namen (_Domänennamen_), wie zum Beispiel `ibm.com`.

Obwohl der grundlegende Ansatz von DNS recht einfach ist, kann die Verwaltung und Speicherung der Datensätze für Ihre verschiedenen Domänen aufwändig sein, wenn kein komfortables Verfahren hierfür zur Verfügung steht.

IBM Cloud DNS bietet den Kunden einen zentralen Standort zum Anzeigen und Verwalten ihrer Domänen durch eine grundlegende DNS-Managementschnittstelle sowie die Option zum Verwalten von Reverse DNS und sekundärem DNS an einer zentralen Position, ganze ohne Kosten für den Kunden.

Darüber hinaus stellt IBM Cloud eine Suite mit zusätzlichen [Netztools](https://console.bluemix.net/docs/infrastructure/network-tools/getting-started.html#getting-started-with-network-tools) bereit. Spezielle Anweisungen für die Verwendung unserer DNS-Schnittstelle im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/) finden Sie [in diesem Dokument](https://github.ibm.com/Bluemix-Docs/dns/blob/staging/using-the-dns-interface.html).

## Funktionsweise
Im Grunde arbeiten die {{site.data.keyword.BluSoftlayer_notm}}-DNS-Funktionen wie andere verfügbare DNS-Managementtools. Sie können mit vorhandenen DNS-Datensätzen interagieren und diese bearbeiten, neue Datensätze hinzufügen und Informationen für Reverse DNS aktualisieren. Im Vergleich zu anderen DNS-Management-Services und zum manuellen DNS-Management bietet {{site.data.keyword.BluSoftlayer_notm}} einen zentralen und zuverlässigen Standort, an dem alle Ihre Daten gespeichert werden.

Als zusätzlichen Service stellt {{site.data.keyword.BluSoftlayer_notm}} den berechtigten Kunden kostenlos sekundäre DNS-Zonen zur Verfügung, um ihre primären DNS-Datensätze vor Datenverlust oder Knotenfehlern zu schützen.

## Vorgehensweise beim DNS-Management
Die meisten Benutzer verwalten Ihre primäre DNS, Reverse DNS und sekundäre DNS in unserem [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/). Unser Portal ermöglicht die Steuerung aller DNS-Managementaktionen per Mausklick.

Alternativ können Sie DNS-Interaktionen mit der IBM Cloud SoftLayer-API (SLAPI) ausführen. Die Funktionsweisen der API und der Portalbenutzerschnittstelle sind nahezu identisch. Wenn Sie jedoch mehrere DNS-Datensätze auf einmal bearbeiten möchten, gilt im Kundenportal eine Begrenzung auf maximal 20 Datensätze, während die API mehr Flexibilität bietet. Weitere Informationen zur Interaktion mit DNS über die SLAPI finden Sie [in dieser API-Dokumentation](dns-api.html).


