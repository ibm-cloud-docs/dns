---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-06"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Übersicht über DNS - Ressourcendatensätze

## Abschnitt für Datensatz `A`

Bei der Mehrzahl der Datensätze handelt es sich um Datensätze des Typs **A**. Dieser Datensatztyp bietet die größte Flexibilität, damit Ihre Domänennamen genau auf das von Ihnen gewünschte Ziel verweisen. Jeder Datensatz besteht aus einem Hostnamen und einer IP-Adresse.

**Feld 'Host':** Der Hostname für den betreffenden Datensatz des Typs 'A'. Der Hostname gibt den Teil Ihres vollständig qualifizierten Domänennamens (Fully Qualified Domain Name, FQDN) an, der vor der Angabe _.domain.com_ steht. Beispielsweise enthält www.domain.com den Hostbestandteil "www" (ohne die Anführungszeichen). Die Suchfunktion fügt automatisch die Angabe “.domain.com” an diese Hostzeichenfolge in der Abfrage an. Ein leerer Datensatztyp 'A' (_domain.com_ und nicht _host.domain.com_) kann erstellt werden, indem das Zeichen '@' in das Hostnamensfeld eingegeben wird.

Häufig verwendete Datensätze des Typs 'A' sind beispielsweise 'www.domain.com', 'ftp.domain.com', 'mail.domain.com', 'webmail.domain.com' und 'mysql.domain.com'.

**Feld 'Verweist auf':** In diesem Feld geben Sie die IP-Adresse an, auf die der Hostname verweisen soll.

## Abschnitt für `CNAME`

Datensätze des Typs 'CNAME' verweisen auf Domänennamen anstatt auf IP-Adressen. Der Vorteil bei der Verwendung eines CNAME-Datensatzes besteht darin, dass Sie einen Host auf einen bestimmten Domänennamen verweisen können und anschließend nur die Datensätze A des Zielhosts ändern müssen, damit die Änderung in beiden Domänen vollzogen wird. Diese Methode wird häufig von den Eigentümern mehrerer TLD-Versionen (.com, .net, .org usw.) derselben Domäne angewendet.

Angenommen, Sie sind Eigner der beiden Domänen _domain.com_ und _domain.net_ und möchten, dass die Datensätze auf dieselbe IP verweisen. Sie erstellen CNAME-Datensätze für den Host _www_ von _domain.net_, die auf 'www.domain.com' verweisen. Um anschließend den Host _www_ von _domain.net_ zu ändern, müssen Sie lediglich den Datensatz A von 'www.domain.com' so ändern, dass er auf die neue IP-Adresse verweist. Ihre Änderung wird automatisch für 'www.domain.net' übernommen.

Ein häufiger Fehler bei der Verwendung dieser Methode besteht darin, dass versehentlich die Datensätze für mehrere Domänen geändert werden, obwohl nur eine Domäne geändert werden soll. Daher sollten Sie _unbedingt_ notieren, welche Domänen aufeinander verweisen. 

**Feld 'Host':** Der Hostname für den jeweiligen CNAME-Datensatz. Der Hostname ist der Teil Ihres FQDN, der der Zeichenfolge '.domain.com' vorangestellt wird. Beispiel: 'www.domain.com' enthält den Hostbestandteil “www” (ohne die Anführungszeichen). Die Suchfunktion fügt automatisch die Angabe “.domain.com” an diese Hostzeichenfolge in der Abfrage an. Ein leerer Datensatz A (_domain.com_ und nicht _host.domain.com_) kann erstellt werden, indem das Zeichen '@' in das Hostnamensfeld eingetragen wird.

**Feld 'Verweist auf':** Der Name, auf den der Datensatz verweist. _Dieses Feld muss einen Domänennamen enthalten (keine IP-Adresse)._ Der Domänenname muss ebenfalls mit einem Punkt enden. Andernfalls springt der Domänendatensatz beim Abfragen zum nächsten Punkt in der Zonendatei.

## Abschnitt für `MX`

Im Abschnitt für MX wird die Zustellung von E-Mails verarbeitet.

**Feld 'Priorität':** In diesem Bereich können Sie Ihre Vorgaben für einen einzelnen MX-Datensatz festlegen. MX-Datensätze werden nacheinander von der niedrigsten bis zur höchsten Priorität verarbeitet. Beispiel: Wenn Sie zwei E-Mail-Server oder einen E-Mail-Server und einen E-Mail-Spooler verwenden, ordnen Sie dem Haupt-E-Mail-Server die niedrigere Priorität zu und dem Backup-E-Mail-Server (oder E-Mail-Spooler) die höhere Priorität.

**Feld 'Host':** Hier kann ein E-Mail-Hostname angegeben werden. In den meisten Fällen ist dies jedoch nicht erforderlich. Stattdessen wird empfohlen, einen leeren Host (mit '@' als Hostname) zu erstellen, der auf Ihren E-Mail-Server verweist.

**Feld 'Verweisziel':** Die Adresse des E-Mail-Servers. In diesem Feld wird häufig angegeben, dass der E-Mail-Hostname, den Sie im Abschnitt für den Datensatz A erstellt haben, als Ziel für Ihre E-Mails verwendet wird.

Ihre MX-Datensätze sollten unbedingt auf einen Domänennamen verweisen und der betreffende Domänenname muss mit einem Punkt enden (wie ein CNAME-Datensatz).

## Abschnitt für `TXT`

Ein TXT-Datensatz kann im Allgemeinen abgefragt werden und gibt Informationen zu einer Domäne zurück. Diese Datensätze können für SPF-Anzeiger verwendet werden, um Port- und Protokollverbindungen zu erstellen oder Informationen zu einer Domäne zurückzugeben. TXT-Datensätze werden häufig mit dem SPF-Protokoll verwendet.

**Name:** Der Host, von dem der TXT-Datensatz abgefragt werden kann.

**Wert:** Die Rückgabe des TXT-Datensatzes (in Anführungszeichen eingeschlossen).
