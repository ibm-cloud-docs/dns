---

copyright: 
  years: 1994, 2020
lastupdated: "2020-03-26"

keywords: dns, domain name registration, dnr

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:external: target="_blank" .external}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
 
# Getting started with Domain Name Registration 
{: #getting-started}

Domain name registration is the process of registering a user-friendly domain name, which identifies one or more IP addresses. {{site.data.keyword.cloud}} Domain Name Registration offers customers a central location from which to view and manage their domains. 
{: shortdesc}

As an additional service, {{site.data.keyword.cloud_notm}} offers secondary domain zones to our customers free of charge, allowing users to back up their primary domain records in the event of data loss or node failure.

{{site.data.keyword.cloud_notm}} domain service functions similarly to any Domain Name System (DNS) management tool that you would use. You have the ability to interact with and edit existing domain records, add new records, and update information about reverse records. The primary benefit of using {{site.data.keyword.cloud_notm}} over another DNS management service, or even managing it yourself, is that you have a central, reliable location in which all of your data is stored.

## Registering a new domain
{: #registering-domain}

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: external} and log in to your account.
1. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. From the Classic Infrastructure menu, select **Services > Domain Registration** to open the Domains page.
1. Choose the **Register** tab.

   Select the **Register Multiple Domains?** option within the **Register** tab if you are registering multiple domains at one time.
   {: tip}

1. Enter the new domain name in the **Domain Name** field.
1. Select the domain type from the **Domain** list.
1. Select the amount of time to reserve the domain from the **Registration Time** list.

    The price for each time period is displayed next to the amount of time and will be charged to the account when the new domain is registered.
    {: note}

1. If registering multiple domains, select the **Add Another** option to populate additional blank fields for more domain entries.

   Select the **Delete** icon to delete an entire entry from the page.
   {: note}

1. Click the **Check Availability** button to check whether the domain names are available. If all domains are available, proceed to the next step. If one or more domains are not available, try again with another domain.
1. Click the **Continue** button to register the domain.

## Next steps
{: #getting-started-next-steps}

* Manage your primary, secondary, reverse domains using the [DNS interface](/docs/dns?topic=dns-how-to-use-the-dns-interface).
* Learn more about the [Domains API](/docs/dns?topic=dns-getting-started-with-the-dns-api).
