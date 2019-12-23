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


# Name server FAQs
{:#nameserver-faqs}

## What are the IBM Cloud name server addresses?
{:#what-are-the-ibm-cloud-name-server-addresses}

We have two addresses for Authoritative Name Servers and two addresses for Resolving Name Servers.

**Authoritative Name Servers**

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

**Resolving Name Servers**

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12


## What is the difference between the public and private name servers at SoftLayer?
{:#what-is-the-difference-public-private-nameserver}

Public name servers act as authoritative name servers for domain names that reside in our DNS servers and are managed through the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/). These servers "answer" and "resolve" domain names to your IP address for the general internet population.

Resolving name servers are located on the private network and act as DNS resolvers for your server. The private resolvers query the internet's root name servers for domain lookups. For example, sending mail from your server requires an NSlookup of the destination domain name. The private DNS servers resolve this information over the private network to keep your bandwidth usage down, reduce the load on the authoritative servers, and offer quick resolution. Private network resolvers are a convenience service for our customers.

## What are my name server options?
{:#what-are-my-name-server-options}

With a Bare Metal Server there are four typical options for name servers:

1. Use your domain name registrar name servers to manage your domain names.
2. Use IBM Cloud name servers to manage your domain names.
3. Use a third party DNS service to manage your domain names.
4. Run your own name servers on your server to manage your domain name.s

For options 1, 2, & 3 you will use name servers of the third party (for example, `ns1.softlayer.com` and `ns2.softlayer.com`). For option number 4, you will use your domain as the name server (`ns1.yourdomain.com` & `ns2.yourdomain.com`). Option number 4 requires you to run DNS services on your server, and you also must register your domain as a name server with your registrar. This registration usually is free, but it requires an additional step beyond the basic domain name registration process.

IBM Cloud offers free Domain Name Registration services that are fully managed through the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/). We highly recommend allowing IBM Cloud to manage your DNS and to act as your name servers, because we have redundant systems, ease of management, and ability to  troubleshoot DNS-related issues quickly.


## How can I run my own name servers?
{:#how-can-i-run-my-own-nameservers}

The easiest way to run and manage your own name servers is to use a control panel tool such as **Plesk** or **cPanel**. Both of these products have built in domain name servers that allow you to add, modify, or delete domain names.

To begin, register your domain name as a name server with your domain name registrar and assign two IP addresses from your server(s) IP ranges.
