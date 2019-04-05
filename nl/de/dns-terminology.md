---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Terminology, Caching, individual DNS servers, DNS resolver

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Terminologie für DNS
{:#dns-terminology}

## Caching und Time to Live
{:#caching-and-time-to-live}

Da ein System wie DNS eine große Menge von Anforderungen generiert, wurde von den Entwicklern das folgende Verfahren bereitgestellt, um die Arbeitslast der einzelnen DNS-Server zu reduzieren:

Wenn ein DNS-Auflöser (Client) eine DNS-Antwort empfängt, wird diese Antwort für einen bestimmte Zeitraum gespeichert. Dieser Zeitraum wird als Time to Live (TTL) oder Lebensdauer bezeichnet. Der Wert für TTL wird vom Administrator des DNS-Servers festgelegt, der die Antwort ausgibt. Wenn eine Antwort im Cache enthalten ist, verwendet der Auflöser diese zwischengespeicherte Antwort. Erst nach Ablauf der TTL (Lebensdauer), oder wenn ein Administrator die Antwort manuell aus dem Speicher des Auflösers löscht, fragt der Auflöse die betreffende Information erneut beim DNS-Server ab.

## Parameter für SOA-Datensatz (SOA = Start of Authority)
{:#soa-record-parameters}

Im Allgemeinen wird die Lebensdauer (Time to Live, TTL) im SOA-Datensatz angegeben. Dieser Datensatz enthält die folgenden Parameter:

### Serial
{:#soa-record-parameters-serial}

Die Revisionsnummer dieser Zonendatei. Erhöhen Sie diese Nummer bei jeder Änderung der Zonendatei, damit die Änderungen auf alle sekundären DNS-Server verteilt werden können.

### Refresh
{:#soa-record-parameters-refresh}

Die Wartezeit in Sekunden, nach der der sekundäre Namensserver im primären Namensserver der Domäne nach einer neuen Kopie einer DNS-Zone sucht. Wenn eine Zonendatei geändert wurde, aktualisiert der sekundäre DNS-Server die Kopie der Zonendatei so, dass sie mit der Zone des primären DNS-Servers übereinstimmt.

### Retry
{:#soa-record-parameters-retry}

Die Wartezeit in Sekunden, nach der der primäre Namensserver (bzw. die primären Namensserver) einer Domäne prüfen sollen, ob die Aktualisierung durch einen sekundären Namensserver fehlschlägt, bevor erneut versucht wird, die Domänenzone mit dem betreffenden Namensserver zu aktualisieren.

### Expire
{:#soa-record-parameters-expire}

Der Zeitraum in Sekunden, in dem ein sekundärer Namensserver (oder mehrere Server) eine Zone als maßgeblich einstuft.

### Minimum
{:#soa-record-parameters-minimum}

Der Gültigkeitszeitraum (in Sekunden) für die Ressourcendatensätze einer Domäne. Dieser Zeitraum wird auch als minimale TTL bezeichnet und kann durch die TTL eines einzelnen Ressourcendatensatzes außer Kraft gesetzt werden.

### TTL (Time to Live, Lebensdauer)
{:#soa-record-parameters-ttl}

Die Gültigkeitszeit (in Sekunden), in der ein Domänenname im lokalen Cache gespeichert bleibt, bevor er ungültig wird und aktualisierte Informationen beim maßgeblichen Namensserver abgefragt werden.
