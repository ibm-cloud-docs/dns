---

copyright:
  years: 1994, 2025
lastupdated: "2025-04-02"

keywords: 

subcollection: dns

---


{{site.data.keyword.attribute-definition-list}}

# About domains
{: #about-domains}

{{site.data.keyword.cloud}} offers domain name service (DNS) management for all customers on the [{{site.data.keyword.cloud_notm}} console](/login).
{: shortdesc}

## Reverse DNS
{: #about-reverse-dns}

Reverse DNS is a method of resolving an IP address into a domain name, just as the domain name system (DNS) resolves domain names into associated IP addresses. One application of reverse DNS is a spam filter. Typically, a spammer uses an invalid IP address that does not match the domain name. A reverse DNS lookup program inputs the IP addresses of incoming messages to a DNS database. If no valid name is found to match the IP address, the server blocks the message. Reverse DNS is also used for things like network troubleshooting calls (such as `ping`) and for network monitoring tools.

## Secondary domains
{: #about-secondary-domains}

A secondary domain is a domain that {{site.data.keyword.cloud_notm}} DNS servers transfer from your server to the IBM authoritative DNS servers: `ns1.softlayer.com` and `ns2.softlayer.com`.  

To set up a secondary domain, you need three pieces of information: the domain, the IP address of the main DNS server that is being transferred from, and how often, in minutes, you want the domain that is transferred.

After a secondary domain is configured, you'll be able to change the main server's IP address and the transfer interval. You are also able to:

* View the domain that is being transferred
* Request a manual transfer
* Convert your secondary domain to a primary domain
* View any error messages that are logged during the transfer.
