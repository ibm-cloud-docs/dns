---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Reverse DNS 

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# About Reverse DNS
{:#about-reverse-dns}

Reverse DNS is a method of resolving an IP address into a domain name, just as the domain name system (DNS) resolves domain names into associated IP addresses. One application of reverse DNS is as a spam filter. Typically, a spammer uses an invalid IP address, one that doesn't match the domain name. A reverse DNS lookup program inputs IP addresses of incoming messages to a DNS database. If no valid name is found to match the IP address, the server blocks the message. Reverse DNS is also used for things like network troubleshooting calls (such as `ping`) and for network monitoring tools.
