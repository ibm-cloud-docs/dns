---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: IBM Cloud name server addresses, Authoritative Name Servers, domain names

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Häufig gestellte Fragen zu Namensservern
{:#nameserver-faqs}

## Wie lauten die Adressen der IBM Cloud-Namensserver?
{:#what-are-the-ibm-cloud-name-server-addresses}

Wir verwenden zwei Adressen für maßgebliche Namensserver und zwei Adressen für auflösende Namensserver.

**Maßgebliche Namensserver**

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

**Auflösende Namensserver**

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12


## Worin unterscheiden sich öffentliche und private Namensserver in SoftLayer?
{:#what-is-the-difference-public-private-nameserver}

Öffentliche Namensserver fungieren als maßgebliche Namensserver für Domänennamen, die sich auf unseren DNS-Servern befinden und über das Kundenportal verwaltet werden. Diese Server übernehmen das "Beantworten" und "Auflösen" von Domänennamen in Ihre IP-Adresse für die allgemeine Internetbelegung.

Auflösende Namensserver befinden sich im privaten Netz und fungieren als DNS-Auflöser für Ihren Server. Die privaten Auflöser fragen die Root-Namensserver des Internets für Domänensuchvorgänge ab. Beispiel: Zum Senden einer E-Mail-Nachricht benötigt Ihr Server einen Befehl 'nslookup' zum Suchen des Zieldomänennamens. Die privaten DNS-Server beziehen diese Informationen über das private Netz, um Ihre Bandbreitennutzung zu minimieren, die Arbeitslast für die maßgeblichen Server zu reduzieren und eine schnelle Auflösung zu ermöglichen. Private Netzauflöser sind ein benutzerfreundlicher Service für unsere Kunden.

## Welche Optionen habe ich für Namensserver?
{:#what-are-my-name-server-options}

Ein Bare-Metal-Server bietet Ihnen vier typische Optionen für Namensserver:

1. Verwenden Sie die Namensserver Ihres Domänennamenregistrators, um Ihre Domänennamen zu verwalten.
2. Verwenden Sie IBM Cloud-Namensserver, um Ihre Domänennamen zu verwalten.
3. Verwenden Sie den DNS-Service eines Drittanbieters, um Ihre Domänennamen zu verwalten.
4. Führen Sie Ihre eigenen Namensserver auf Ihrem Server aus, um Ihre Domänennamen zu verwalten.

Für die Optionen 1, 2 und 3 verwenden Sie Namensserver des Drittanbieters (z. B. `ns1.softlayer.com` und `ns2.softlayer.com`). Für die Option 4 verwenden Sie Ihre eigene Domäne als Namensserver (`ns1.ihredomäne.com` & `ns2.ihredomäne.com`). Für die Option 4 müssen Sie DNS-Services auf Ihrem Server ausführen. Außerdem müssen Sie Ihre Domäne als Namensserver bei Ihrem Registrator registrieren. Diese Registrierung ist in der Regel kostenlos; sie erfordert jedoch einen zusätzlichen Schritt über den grundlegenden Registrierungsprozess für Domänennamen hinaus.

IBM Cloud stellt kostenlose DNS-Services zur Verfügung, die vollständig über das [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/) verwaltet werden. Wir empfehlen dringend die Verwendung von IBM Cloud zum Verwalten Ihres DNS und für Ihre Namensserver, um die Vorteile unserer redundanten Systeme, des hohen Verwaltungskomforts und der Funktionalität für schnelle Fehlersuche bei DNS-bezogenen Problemen zu nutzen.


## Wie kann ich eigene Namensserver ausführen?
{:#how-can-i-run-my-own-nameservers}

Die einfachste Methode zum Ausführen und Verwalten eigener Namensserver ist die Verwendung eines Tools wie **Plesk** oder **cPanel**. Beide Produkte verfügen über integrierte Domänennamensserver, mit denen Sie Domänennamen hinzufügen, ändern oder löschen können.

Registrierten Sie zunächst Ihren Domänennamen bei Ihrem Domänennamenregistrator als einen Namensserver und ordnen Sie zwei IP-Adressen aus den IP-Bereichen Ihres Servers oder Ihrer Server zu.
