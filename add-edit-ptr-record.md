---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Record PTR, IP addresses, Reverse DNS feature

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Add or Edit a PTR (Pointer) Record
{:#add-or-edit-a-ptr-pointer-record}

PTR, or pointer, records resolve IP addresses into hostnames. Users may add PTR Records to be associated with an IP address by using the Reverse DNS feature on the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){:new_window}. Also, PTR Records may be edited in the same way they are added. Follow the steps below to add or edit a PTR Record for a device:

1. Retrieve the **Public IP Address** for the device that will receive the PTR Record from the **Device List**.
1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Reverse DNS Records**.
1. Enter the **Public IP Address** retrieved from the Device List in the **View IP** field.
1. Click anywhere on the row containing the **Reverse Record** details to open the row for edits.
1. Complete or update the fields for the Record based on the table below:

  |Field|Entry|
  |:---|:---|
  |Reverse DNS|The hostname to which the IP Address will resolve.|
  |Reverse TTL|The time to live (TTL) for the new Record|
  |Notes|Any applicable notes regarding the Record|

1. Click the **Update** button to update the record. Click **Cancel** to cancel the action.

## What Happens Next
{:#add-or-edit-a-ptr-pointer-record-next}

After a PTR Record is added, the Public IP Address associated with that record will resolve to the hostname specified in the record. The record may be edited at any time. To remove details from the PTR Record, delete all information from the fields using the **Edit** process.
