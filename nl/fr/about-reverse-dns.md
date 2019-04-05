---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Reverse DNS 

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# A propos du DNS en amont
{:#about-reverse-dns}

Le DNS en amont (ou RDNS) est une méthode de résolution d'une adresse IP dans un nom de domaine, tout comme le système de noms de domaine (DNS) convertit les noms de domaine en adresses IP associées. Un RDNS peut être appliqué en tant que filtre antispam. Généralement, un spammeur utilise une adresse IP non valide qui ne correspond pas au nom de domaine. Un programme de recherche de RDNS entre les adresses IP des messages entrants dans une base de données DNS. Si aucun nom valide n'est trouvé pour correspondre à l'adresse IP, le serveur bloque le message. RDNS est également utilisé pour des opérations telles que des appels de traitement des incidents du réseau (tels que `ping`) et pour des outils de surveillance du réseau.
