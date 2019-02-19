---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"
---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# How to use the DNS interface

Follow these steps to utilize the DNS interface through the IBM Cloud customer portal:

* Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Classic Infrastructure** from the Navigation Menu
* Select **Network->DNS->Forward Zones**
* Select the Domain you wish to manage, or select the **Add DNS Zone** button on the Right side of the page.

## DNS Interface Overview
Working in the DNS Interface on the Customer Portal gives you full capabilities for managing all aspects of your DNS. You can perform every type of DNS management from any screen in the interface, by using the static menu bar at the top of your screen.

## Manage DNS
Upon reaching the DNS interface in the Portal, you will be routed directly to the **Manage DNS** screen, which allows you view, edit, or delete any existing primary DNS associated with your account.

* To add new records simply fill out the fields provided under **Add New Record** and click the **Add Record** button.
* To modify an existing record click on the line containing the record and it will convert to **Edit** mode. Change the settings to the desired values and click **Update**.
* To delete a record, select the Red circle to the right of the record, and then click **Yes** on the prompt.

## Secondary DNS

* Navigate to the [Customer Portal Classic Infrastructure ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Classic Infrastructure** from the Navigation Menu
* Select **Network->DNS->Secondary Zones**

From this screen you can add or modify secondary DNS settings.

* To add a new record, select **Add Zone**, fill in the fields and select **Add**.
* To remove a Secondary DNS record, or convert it to a Primary record, use the **Actions** drop-down on the right of the page and choose the appropriate option.

## Reverse DNS

Follow these steps to utilize the DNS interface through Portal navigation:

* Navigate to the [Customer Portal Classic Infrastructure ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Classic Infrastructure** from the Navigation Menu
* Select **Network->DNS->Reverse Records**
* In the dropdown menu, either select or type the IP address for which you wish to change Reverse DNS, then select **View IP**
  * To add the record, enter the Hostname you wish to use for the reverse DNS entry
  * Set the TTL (Time to Live) for the record.
  * Once you are certain of the information, select **Save**.

You can modify an entire subnet by clicking **Edit RDNS for all IPs in this Subnet** on the right of the page.

* From this page, select the line for the IP you wish to update
* Enter the information into the fields, and then select **Update**. The "notes" field is optional.

<!--## Propagation Check

* Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network->Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
