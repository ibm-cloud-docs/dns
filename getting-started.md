---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-05-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Getting Started with DNS

The internet's Domain Name System (DNS) is a method of translating IP addresses that servers and routers recognize into user-friendly, given names called _domain names_ (for example, `ibm.com`).

While the concept of DNS is simple, managing and storing records for your various domains can become quite tedious if there isn’t a convenient method to do so.

IBM Cloud DNS offers customers a central location from which to view and manage their domains, by using our basic DNS management interface. It also gives users the option to manage reverse and secondary DNS in the same location, free of charge.

IBM Cloud also offers a suite of additional [network tools](https://console.bluemix.net/docs/infrastructure/network-tools/getting-started.html#getting-started-with-network-tools). For specific instructions about using our DNS interface through the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/), [see this document](using-the-dns-interface.html).

## How it Works
At a basic level, {{site.data.keyword.BluSoftlayer_notm}} DNS functions similarly to any DNS management tool that you would use. You have the ability to interact with and edit existing DNS records, add new records, and update information about reverse DNS. The primary benefit of using {{site.data.keyword.BluSoftlayer_notm}} over another DNS management service or even managing it yourself is that you have a central, reliable location in which all of your data is stored.

As an additional service, {{site.data.keyword.BluSoftlayer_notm}} offers secondary DNS zones to our customers free of charge, allowing users to back up their primary DNS records in the event of data loss or node failure.

## How to Manage DNS
Most users manage their primary, reverse and secondary DNS using our [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). The Portal is our point and click interface to manage all things DNS.

You also have the option to use the IBM Cloud SoftLayer API (SLAPI) for DNS interactions. The functionality of the API compared to our Portal UI is almost identical. However, if you are editing DNS records in bulk, the Customer Portal provides bulking in sets up to a maximum of 20, while the API offers more flexibility. For more information about interacting with DNS using the SLAPI, refer to [this API documentation](dns-api.html).


