---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-13"

keywords: DNS servers, fast domain name resolution, DNS FAQ

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}


# Häufig gestellte Fragen zu DNS
{:#dns-faq}

## Was sind die DNS-Server?
{:#what-are-dns-servers}
{: faq}

161.26.0.10 und 161.26.0.11

## Was sind lokale DNS-Auflöser?
{:#what-are-local-dns-resolvers}
{: faq}

Die lokalen auflösenden Namensserver in unserem privaten Netz sind:

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Diese Namensserver führen die schnelle Auflösung von Domänennamen durch, ohne Ihre öffentliche Bandbreitenzuordnung auszuschöpfen. Halten Sie bei der Verwendung die korrekte Vorgehensweise zum Hinzufügen auflösender Namensserver für Ihr Betriebssystem ein.

## Wie lauten die Adressen der {{site.data.keyword.BluSoftlayer_notm}}-Namensserver?
{:#what-are-name-server-addresses}
{: faq}

Wir verwenden zwei Adressen für maßgebliche Namensserver und zwei Adressen für auflösende Namensserver.

### Maßgebliche Namensserver
{:#authoratative-name-servers}

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### Auflösende Namensserver
{:#resolving-name-servers}

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

Diese lokalen auflösenden Namensserver befinden sich in unserem privaten Netz, damit Ihre öffentliche Bandbreitenzuordnung nicht ausgeschöpft wird. 

## Welche IBM Cloud-DNS-Server antworten auf meine sekundären Domänen?
{:#what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}

Die maßgeblichen, für IPv aktivierten {{site.data.keyword.BluSoftlayer_notm}} Anycast-DNS-Server antworten auf Ihre sekundären Domänen. Diese Server verwenden die folgenden Adressen:

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## Welche IP-Adressen werden für Übertragungen meiner sekundären Domänenzonen verwendet?
{:#which-ipaddresses-secondary-domain-zone-transfers}
{: faq}

Übertragungen für Ihre sekundären Domänen stammen von einer der vier folgenden IP-Adressen:

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## Worin unterscheiden sich öffentliche und private Namensserver?
{:#public-v-private-nameservers}
{: faq}

Unsere öffentlichen Namensserver fungieren als maßgebliche Namensserver für Domänennamen, die sich auf unseren DNS-Servern befinden und über das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/) verwaltet werden. Diese Server übernehmen das "Beantworten" und "Auflösen" von Domänennamen in Ihre IP-Adresse für die allgemeine Internetbelegung.

Unsere auflösenden Namensserver befinden sich im privaten Netz und fungieren als DNS-Auflöser für Ihren Server. Die privaten Auflöser fragen die Root-Namensserver des Internets für Domänensuchvorgänge ab. Beispiel: Zum Senden einer E-Mail-Nachricht benötigt Ihr Server einen Befehl 'nslookup' zum Suchen des Zieldomänennamens. Die privaten DNS-Server beziehen diese Informationen über das private Netz, um Ihre Bandbreitennutzung zu minimieren, die Arbeitslast für die maßgeblichen Server zu reduzieren und eine schnelle Auflösung zu ermöglichen. Private Netzauflöser sind ein benutzerfreundlicher Service für unsere Kunden.

## Welche Optionen habe ich für Namensserver?
{:#what-are-my-name-server-options-faq}
{: faq}

Ein Bare-Metal-Server bietet Ihnen vier typische Optionen für Namensserver:

* Verwenden Sie die Namensserver Ihres Domänennamenregistrators, um Ihre Domänennamen zu verwalten.
* Verwenden Sie {{site.data.keyword.BluSoftlayer_notm}}-Namensserver, um Ihre Domänennamen zu verwalten.
* Verwenden Sie den DNS-Service eines Drittanbieters, um Ihre Domänennamen zu verwalten.
* Führen Sie Ihre eigenen Namensserver auf Ihrem Server aus, um Ihre Domänennamen zu verwalten.

Für die ersten drei Optionen verwenden Sie Namensserver des Drittanbieters (z. B. `ns1.softlayer.com` und `ns2.softlayer.com`). Bei der letzten Option wird Ihre Domäne als Namensserver verwendet (z. B. `ns1.ihredomäne.com` & `ns2.ihredomäne.com`) und Sie müssen DNS-Services auf Ihrem Server ausführen. Außerdem müssen Sie Ihre Domäne als Namensserver bei Ihrem Registrator registrieren. Die Registrierung für Nameserver ist in der Regel kostenlos; sie erfordert jedoch einen zusätzlichen Schritt über den grundlegenden Registrierungsprozess für Domänennamen hinaus.

Für unsere Kunden stehen kostenlose DNS-Services zur Verfügung, die vollständig über das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/) verwaltet werden. Wir empfehlen dringend die Verwaltung Ihrer DNS und Namensserver mit {{site.data.keyword.BluSoftlayer_notm}}, um die Vorteile unserer redundanten Systeme, des hohen Verwaltungskomforts und der Funktionalität für schnelle Fehlersuche bei DNS-bezogenen Problemen zu nutzen.

## Wie kann ich Reverse DNS einrichten?
{:#how-do-i-setup-reverse-dns}
{: faq}

Reverse DNS kann in unserem [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/) eingerichtet werden. Anweisungen zum Einrichten Ihres Reverse DNS finden Sie im Abschnitt [Reverse DNS-Datensatz aktualisieren](/docs/infrastructure/dns?topic=dns-update-reverse-dns-record).


## Wie lange dauert die Weitergabe von DNS-Änderungen?
{:#how-long-for-dns-changes-propagate}
{: faq}

Die Laufzeiten für die Weitergabe von DNS-Änderungen hängen von der Einstellung der Lebensdauer (Time-to-Live (TTL) für den DNS-Datensatz ab.

Die Standardlebensdauer ist ein Tag, d. h. Änderungen an einem Domänennamen werden innerhalb eines Tages im gesamten Internet verbreitet. Die Lebensdauer (TTL) kann verkürzt werden, wenn häufig Änderungen vorgenommen werden sollen. Beachten Sie dabei Folgendes: Je kürzer die Lebensdauer, umso höher die Arbeitslast für den Namensserver. Höhere Arbeitslasten können längere Antwortzeiten für Endbenutzer nach sich ziehen und damit die Gesamtzufriedenheit der Endbenutzer beeinträchtigen.

Je größer der TTL-Wert, umso höher die DNS-Leistung aufgrund der lokalen ISP-Zwischenspeicherung. Je kleiner der TTL-Wert, umso geringer die DNS-Leistung aufgrund des höheren Aufwands für die Namensauflösung.

Um den TTL-Wert zu prüfen, überprüfen Sie den SOA-Datensatz (SOA = Start of Authority) für die Domäne. Ein hilfreiches Tool zum Überprüfen der Domäneninformationen wird von [CentralOps.net ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://centralops.net/co/) angeboten.

Der TTL-Wert wird in Sekunden angegeben. Teilen Sie den TTL-Wert durch 60, um ihn in Minuten umzurechnen, oder durch 3.600, um ihn in Stunden umzurechnen.


## Wie lange dauert es nach dem Übertragen einer Domäne, bis die Domäne und die Änderungen angezeigt werden?
{:#how-long-transfer-change-visiblity}
{: faq}

Ihre Domäne und/oder die an der Domäne vorgenommenen Änderungen sind auf IBM Cloud-DNS-Servern sichtbar, sobald die Übertragung abgeschlossen ist. Aufgrund der Weitergabefunktionen von DNS sind die Änderungen erst nach einer gewissen Verzögerung auf anderen DNS-Servern sichtbar.

## Kann ich AXFR-Anforderungen im privaten Netz ausführen?
{:#axfr-request-private-network}
{: faq}

{{site.data.keyword.BluSoftlayer_notm}} bietet derzeit keine Unterstützung für AXFR-Anforderungen im privaten Netz. Alle AXFR-Anforderungen müssen im öffentlichen Netz ausgeführt werden.
