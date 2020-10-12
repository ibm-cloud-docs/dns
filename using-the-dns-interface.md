---

copyright:
  years: 1994, 2020
lastupdated: "2020-03-26"

keywords:

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:term: .term}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:external: target="_blank" .external}
{:generic: data-hd-programlang="generic"}
{:download: .download}
{:DomainName: data-hd-keyref="DomainName"}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Using the DNS interface
{:#how-to-use-the-dns-interface}
{: help}
{: support}

In the DNS interface, you have the ability to manage **Forward Zones**, **Secondary Zones**, and **Reverse Records**.
{:shortdesc}

## Forward zones
{: #forward-zones}

To manage forward zones:

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Forward Zones**
1. Select the domain you want to manage, or select the **Add DNS zone** button on the right side of the page.

## Secondary zones
{:#secondary-dns}

To manage secondary zones:

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Secondary Zones**. From this page you can add or modify secondary DNS settings.
1. To add a new record, select **Add Zone**, complete the fields and select **Add**.
1. To remove a Secondary DNS record, or convert it to a primary record, use the **Actions** list menu on the right of the page and choose the appropriate option.

## Reverse records
{:#reverse-dns}

To manage reverse records:

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Reverse Records**.
1. In the list menu, either select or type the IP address for which you wish to change reverse DNS, then select **View IP**
1. To add the record, enter the Hostname you want to use for the reverse DNS entry.
1. Set the TTL (Time to Live) for the record.
1. After you are certain of the information, select **Save**.

You can modify an entire subnet by clicking **Edit RDNS for all IPs in this Subnet** on the right of the page.

1. From this page, select the line for the IP you want to update.
1. Enter the information into the fields, and then select **Update**. The "notes" field is optional.
