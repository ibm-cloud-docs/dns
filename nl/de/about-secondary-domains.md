---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary Domains, secondary domain, IBM Cloud DNS servers transfer

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informationen zu sekundären Domänen
{:#about-secondary-domains}

Eine sekundäre Domäne ist eine Domäne, die {{site.data.keyword.BluSoftlayer_notm}}-DNS-Server von Ihrem Server auf unsere maßgeblichen DNS-Server `ns1.softlayer.com` und `ns2.softlayer.com` übertragen.  Sie können im Portal eine sekundäre Domäne konfigurieren, indem Sie auf **<span style="text-decoration: underline">Domain Name System</span>** im Ordner **<span style="text-decoration: underline">Öffentliches Netz</span>** klicken, anschließend auf den Link **<span style="text-decoration: underline">Sekundäres DNS</span>** und danach auf **<span style="text-decoration: underline">Sekundären DNS-Datensatz hinzufügen</span>**.

Zum Einrichten einer sekundären Domäne sind drei Einzelinformationen erforderlich: die Domäne, die *IP-Adresse des Master-DNS-Servers*, der als Übertragungsquelle dient, und wie häufig (angegeben in Minuten) die Domäne übertragen werden soll.<br/>
Sobald eine sekundäre Domäne konfiguriert ist, können Sie die IP-Adresse des Master-Servers und das Übertragungsintervall ändern.  Außerdem können Sie während der Übertragung die Domäne anzeigen, eine manuelle Übertragung anfordern, Ihre sekundäre Domäne in eine primäre Domäne umwandeln und Fehlernachrichten anzeigen, die während des Übertragungsprozesses protokolliert wurden.
