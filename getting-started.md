---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-03"

keywords: IBM Cloud DNS, DNS

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Getting started with Domain Name Registration
{: #getting-started}

The internet's Domain Name System (DNS) is a method of translating IP addresses that servers and routers recognize into user-friendly, given names called _domain names_ (for example, `ibm.com`).

While the concept of DNS is simple, managing and storing records for your various domains can become quite tedious if there isn’t a convenient method to do so.

{{site.data.keyword.cloud_notm}} Domain Name Registration offers customers a central location from which to view and manage their domains, by using our basic DNS management interface. It also gives users the option to manage reverse and secondary DNS in the same location, free of charge.

{{site.data.keyword.cloud_notm}} also offers a suite of additional [network tools](/docs/infrastructure/network-tools?topic=network-tools-getting-started). For specific instructions about using our Domain Name Registration interface through the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){:external}, see [How to use the DNS interface](/docs/infrastructure/dns?topic=dns-how-to-use-the-dns-interface).

## How it works
{: #how-dns-works}

At a basic level, {{site.data.keyword.cloud_notm}} Domain Name Registration functions similarly to any DNS management tool that you would use. You have the ability to interact with and edit existing DNS records, add new records, and update information about reverse DNS. The primary benefit of using {{site.data.keyword.cloud_notm}} over another DNS management service or even managing it yourself is that you have a central, reliable location in which all of your data is stored.

As an additional service, {{site.data.keyword.cloud_notm}} offers secondary DNS zones to our customers free of charge, allowing users to back up their primary DNS records in the event of data loss or node failure.

## How to Manage DNS
{: #how-to-manage-dns}

Most users manage their primary, reverse, and secondary DNS using our [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/). The console is our point and click interface to manage all things DNS.

You also have the option to use the IBM Cloud SoftLayer API (SLAPI) for DNS interactions. The functionality of the API compared to our console UI is almost identical. However, if you are editing DNS records in bulk, the console provides bulking in sets up to a maximum of 20, while the API offers more flexibility. For more information about interacting with DNS using the SLAPI, refer to [this API documentation](/docs/infrastructure/dns?topic=dns-getting-started-with-the-dns-api#getting-started-with-the-dns-api).
