---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-12-13"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

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

# How to use the DNS interface
{:#how-to-use-the-dns-interface}

Follow these steps to utilize the DNS interface through the {{site.data.keyword.cloud}} console:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > >Forward Zones.**
1. Select the Domain you wish to manage, or select the **Add DNS Zone** button on the right side of the page.

## DNS Interface Overview
{:#dns-interface-overview}
Working in the DNS Interface on the console gives you full capabilities for managing all aspects of your DNS. You can perform every type of DNS management from any screen in the interface, by using the static menu bar at the top of your screen.

## Manage DNS
{:#manage-dns}
Upon reaching the DNS interface in the console, you will be routed directly to the **Manage DNS** screen, which allows you view, edit, or delete any existing primary DNS associated with your account.

* To add new records simply fill out the fields provided under **Add New Record** and click the **Add Record** button.
* To modify an existing record click on the line containing the record and it will convert to **Edit** mode. Change the settings to the desired values and click **Update**.
* To delete a record, select the delete icon to the right of the record, and then click **Yes** on the prompt.

## Secondary DNS
{:#secondary-dns}

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Secondary Zones**.



From this screen you can add or modify secondary DNS settings.

* To add a new record, select **Add Zone**, fill in the fields and select **Add**.
* To remove a Secondary DNS record, or convert it to a Primary record, use the **Actions** list menu on the right of the page and choose the appropriate option.

## Reverse DNS
{:#reverse-dns}

Follow these steps to utilize the DNS interface through console navigation:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Reverse Records**.
1. In the list menu, either select or type the IP address for which you wish to change Reverse DNS, then select **View IP**
  * To add the record, enter the Hostname you wish to use for the reverse DNS entry
  * Set the TTL (Time to Live) for the record.
  * Once you are certain of the information, select **Save**.

You can modify an entire subnet by clicking **Edit RDNS for all IPs in this Subnet** on the right of the page.

* From this page, select the line for the IP you wish to update
* Enter the information into the fields, and then select **Update**. The "notes" field is optional.
