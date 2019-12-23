---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-12-13"

keywords: Secondary Domains, secondary domain, IBM Cloud DNS servers transfer

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# About Secondary Domains
{:#about-secondary-domains}

A secondary domain is a domain that {{site.data.keyword.cloud_notm}} DNS servers transfer from your server to our Authoritative DNS servers, `ns1.softlayer.com` and `ns2.softlayer.com`.  You can configure a secondary domain in the console by clicking on **Domain Name System** in the **Public Network** folder in the console, clicking on the **Secondary DNS** link, and finally, clicking on **Add Secondary DNS Record**.

To set up a secondary domain, you'll need three pieces of information: the domain, the *IP address of the master DNS server* we're transferring from and how often, in minutes, you'd like the domain transferred.

Once a secondary domain is configured, you'll have the ability to change the master server's IP address and the transfer interval.  You will also be able to view the domain as we're transferring, request a manual transfer, convert your secondary domain to a primary domain, and view any error messages we logged during the transfer process.
