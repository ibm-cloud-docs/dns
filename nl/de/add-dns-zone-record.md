---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS-Zonendatensatz hinzufügen

Nach dem [Hinzufügen einer DNS-Zone](add-dns-zone.html) können jederzeit Datensätze in der Zone hinzugefügt werden. Dazu gehören die folgenden Datensätze:

* A (Hostdatensätze)
* AAAA (Hostdatensätze)
* CNAME (Aliasdatensätze)
* MX (Mailaustauschdatensätze)
* TXT (Textdatensätze)
* SRV (Servicedatensätze)

Führen Sie die folgenden Schritte aus, um einen DNS-Zonendatensatz hinzuzufügen:

* Navigieren Sie zur Anzeige für die gewünschte **DNS-Zone**. Weitere Informationen finden Sie unter [Anzeige 'DNS-Zonen' verwenden](use-dns-zones-screen.html).
* Wählen Sie die DNS-Zone aus, zu der Sie einen Datensatz hinzufügen möchten.
* Wählen Sie den gewünschten **Ressourcentyp** in der Dropdown-Liste **Ressourcentyp** aus.
* Füllen Sie die übrigen Felder für den neuen Datensatz aus. Weitere Informationen finden Sie in der nachfolgenden Tabelle:<br/><br/><table border="1"><tbody><tr><th>Datensatztyp</th><th>Feld</th><th>Eintrag</th></tr><tr><td rowspan="3">A (Host), AAAA (Host) oder CNAME (Alias)</td><td>Host</td><td>Geben Sie den <strong>Hostnamen</strong> ein.</td></tr><tr><td>Verweist auf</td><td>Geben Sie die <strong>IP-Adresse</strong> ein, auf die der Hostdatensatz verweist.</td></tr><tr><td>TTL</td><td>Wählen Sie die Lebensdauer (Time to Live, TTL) in der Dropdown-Liste aus. Der Standardwert für TTL ist 15 Minuten.</td></tr><tr><td rowspan="4">MX (Mail Exchange)</td><td>Priorität</td><td>Geben Sie die <strong>Priorität</strong> für den Zielhost ein. Je kleiner die Zahl, umso höher die Priorität.</td></tr><tr><td>Host</td><td>Geben Sie den <strong>Hostnamen</strong> ein.</td></tr><tr><td>GOES</td><td>Geben Sie den Alias (<strong>CNAME</strong>) des E-Mail-Servers ein. Dieser Name wird in der Regel als 'mail.example.com' dargestellt.</td></tr><tr><td>TTL</td><td>Wählen Sie die Lebensdauer (Time to Live, TTL) in der Dropdown-Liste aus. Der Standardwert für TTL ist 15 Minuten.</td></tr><tr><td rowspan="3">TXT (Text)</td><td>Name</td><td>Geben Sie das Zeichen <strong>@</strong> oder den <strong>Domänennamen</strong> ein.</td></tr><tr><td>Wert</td><td>Geben Sie den <strong>Datensatz</strong> zum Überprüfen der entsprechenden E-Mail-Abschlussrechte für eine Domäne oder IP-Adresse ein.</td></tr><tr><td>TTL</td><td>Wählen Sie die Lebensdauer (Time to Live, TTL) in der Dropdown-Liste aus. Der Standardwert für TTL ist 15 Minuten.</td></tr><tr><td rowspan="8">SRV (Servicedatensatz)</td><td>Service</td><td>Geben Sie den <strong>symbolischen Namen</strong> des gewünschten Service ein.</td></tr><tr><td>Protokoll</td><td>Wählen Sie in der Dropdown-Liste <strong>Protokoll</strong> das Protokoll aus, das verwendet wird.</td></tr><tr><td>Priorität</td><td>Geben Sie die <strong>Priorität</strong> für den Zielhost ein. Je kleiner die Zahl, umso höher die Priorität.</td></tr><tr><td>Gewichtung</td><td>Geben Sie die <strong>relative Gewichtung</strong> für Datensätze mit gleicher Priorität ein.</td></tr><tr><td>Port</td><td>Geben Sie den <strong>TCP- oder UPD-Port</strong> ein, über den der Service erreichbar sein soll.</td></tr><tr><td>Host (optional)</td><td>Geben Sie den <strong>Hostnamen</strong> für den Service ein.</td></tr><tr><td>Ziel</td><td>Geben Sie den <strong>kanonischen Hostnamen</strong> der Maschine ein, die den Service bereitstellt.</td></tr><tr><td>TTL</td><td>Wählen Sie die Lebensdauer (Time to Live, TTL) in der Dropdown-Liste aus. Der Standardwert für TTL ist 15 Minuten.</td></tr></tbody></table><br/>
* Wählen Sie die Schaltfläche **Datensatz hinzufügen** aus, um den neuen Zonendatensatz hinzuzufügen.

## Weitere Schritte

Nach dem Hinzufügen wird der Zonendatensatz im Abschnitt **Vorhandene Datensätze** der Anzeige aufgelistet. Sie können den Zonendatensatz jederzeit [bearbeiten](edit-dns-zone-record.html) oder löschen.
