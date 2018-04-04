---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-06"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Häufig gestellte Fragen zu sekundären Domänen

## Welche IBM Cloud-DNS-Server reagieren auf meine sekundären Domänen?

Die maßgeblichen, für IPv6 aktivierten DNS-Server von IBM Cloud Anycast:

 * ns1.softlayer.com
 * ns2.softlayer.com

## Aus welcher Quelle stammen die Zonenübertragungen?

Übertragungen Ihrer sekundären Domänen stammen von einer der folgenden vier IP-Adressen:

  * 66.228.118.67
  * 67.228.119.235
  * 208.43.119.235
  * 12.96.161.249

## Wie lange dauert es nach dem Übertragen einer Domäne, bis die Domäne oder Änderungen der Domäne angezeigt werden?

Die Domäne und/oder die an der Domäne vorgenommenen Änderungen sind auf IBM Cloud-DNS-Servern sichtbar, sobald die Übertragung abgeschlossen ist. Aufgrund der Caching- und Weitergabefunktionen von DNS sind die Änderungen erst nach einer gewissen Verzögerung auf anderen DNS-Servern sichtbar.  

## Werden Benachrichtigungen über Zonenänderungen unterstützt?

Gegenwärtig werden keine Benachrichtigungen unterstützt.

## Wie schnell wird auf die Schaltfläche 'Jetzt übertragen' reagiert?

Nach dem Klicken auf die Schaltfläche 'Jetzt übertragen' wird die betreffende Domäne zu Beginn der nächsten Minute übertragen.

## Kann ein Master im privaten Netz konfiguriert werden, oder muss das öffentliche Netz verwendet werden?

Dies ist gegenwärtig nicht im privaten Netz möglich. Alle AXFR-Anforderungen müssen im öffentlichen Netz ausgeführt werden.

## Werden Slaves entfernt, wenn der Master nach einer bestimmten Anzahl von Tagen nicht verfügbar ist?

Es werden keine weiteren Übertragungsversuche für eine Domäne durchgeführt, wenn der zugehörige Master über einen längeren Zeitraum inaktiv oder fehlerhaft konfiguriert ist. Das Portal stellt Rückmeldung für Kunden (auf der Registerkarte 'Fehlernachrichten') und eine Methode zum Reaktivieren einer Domäne (auf der Registerkarte 'Manuelle Zonenübertragung') bereit, falls eine Zone aufgrund von Übertragungsfehlern inaktiviert wird.

## Ist 1 Minute der niedrigste Wert für die Übertragungshäufigkeit?

Ja.

## Wenn die Häufigkeit auf den Wert '1920 Minuten' gesetzt und anschließend in den Wert '10 Minuten' geändert wird, müssen dann die 1920 Minuten abgelaufen sein, bevor der neue Wert wirksam wird?

Nein. Das System berechnet die Warteschlange für die erneute Übertragung, indem der Häufigkeitswert zum Zeitpunkt des letzten Übertragungsversuchs addiert wird. Dies bedeutet, wenn Sie den Häufigkeitswert 1920 in 10 ändern, erfolgt der nächste Übertragungsversuch nach Ablauf von mindestens 10 Minuten seit dem vorherigen Versuch und danach alle 10 Minuten.
