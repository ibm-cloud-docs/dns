---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary Domains, secondary domain, IBM Cloud DNS servers transfer

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informazioni sui domini secondari
{:#about-secondary-domains}

Un dominio secondario è un dominio che i server DNS di {{site.data.keyword.BluSoftlayer_notm}} trasferiscono dal tuo server ai tuoi server DNS autorevoli, `ns1.softlayer.com` e `ns2.softlayer.com`.  Puoi configurare un dominio secondario nel portale facendo clic su **<span style="text-decoration: underline">Domain Name System</span>** nella cartella **<span style="text-decoration: underline">Public Network</span>** (Rete pubblica) nel Portale, facendo clic sul link **<span style="text-decoration: underline">Secondary DNS</span>** (DNS secondario) e, infine, facendo clic su **<span style="text-decoration: underline">Add Secondary DNS Record</span>** (Aggiungi record DNS secondario).

Per configurare un dominio secondario, ti serviranno tre informazioni: il dominio, l'*indirizzo IP del server DNS master* da cui stiamo eseguendo il trasferimento e la frequenza di trasferimento del dominio da te desiderata, espressa in minuti.<br/>
Una volta che un dominio secondario è stato configurato, potrai modificare l'indirizzo IP del server master e l'intervallo di trasferimento.  Potrai anche visualizzare il dominio mentre lo trasferiamo, richiedere un trasferimento manuale, convertire il tuo dominio secondario in un dominio primario e visualizzare gli eventuali messaggi di errore che registriamo nei log durante il processo di trasferimento.
