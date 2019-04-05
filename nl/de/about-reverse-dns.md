---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Reverse DNS 

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informationen zu Reverse DNS
{:#about-reverse-dns}

Reverse DNS ist eine Methode zum Auflösen einer IP-Adresse in einen Domänennamen, ähnlich wie beim Auflösen von Domänennamen in die zugehörigen IP-Adressen durch das Domain Name System (DNS). Eine Anwendungsmöglichkeit für Reverse DNS ist das Einrichten eines Spamfilters. Ein Spammer nutzt in der Regel eine ungültige IP-Adresse, die nicht mit dem Domänennamen übereinstimmt. Ein Programm für Reverse-DNS-Lookup gibt IP-Adressen aus ankommenden Nachrichten in eine DNS-Datenbank ein. Wenn kein gültiger Name für die IP-Adresse gefunden wird, blockiert der Server die Nachricht. Reverse DNS wird darüber hinaus in Aufrufen für die Behebung von Netzfehlern (z. B. `ping`) und für Netzüberwachungstools verwendet.
