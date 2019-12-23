---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone Record, Update DNS Zone Record, edit dns zone record, add dns zone record, delete dns zone record

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Managing DNS Zone Records
{: #manage-dns-zone-records}
This section details how to add, edit, and delete DNS Zone Records.

## Add a DNS Zone Record
{: #add-a-dns-zone-record}

After [adding a DNS Zone](/docs/infrastructure/dns?topic=dns-manage-dns-zones#add-a-dns-zone), Records may be added to the zone at any time. These records include:

* A (Host) Records
* AAAA (Host) Records
* CNAME (Alias) Records
* MX (Mail Exchange) Records
* TXT (Text) Records
* SRV (Service) Records

Follow the steps below to add a DNS Zone Record:

* Navigate to the **DNS Zone** screen. Refer to [Using the DNS Zones Screen](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens).
* Select the DNS Zone to which the record will be added.
* Select the desired **resource type** from the **Resource Type** list.
* Complete the remaining fields for the new Record. Refer to the table below for more information:

| Record Type|Field|Entry|
|:-----|:-----|:-----|
|A (Host), AAAA (Host) or CNAME (Alias) |Host|Enter the **Host Name**.|
|A (Host), AAAA (Host) or CNAME (Alias) | Points To|Enter the **IP Address** to which the Host Record points.|
|A (Host), AAAA (Host) or CNAME (Alias) |TTL|Select the Time to Live (TTL) from the list menu. TTL defaults to 15 minutes.|
|MX (Mail Exchange) |Priority|Enter the **Priority** of the target host. The lower the number, the higher the priority.|
|MX (Mail Exchange) |Host|Enter the **Host Name**.|
|MX (Mail Exchange) |Goes|Enter the **CNAME** of the mail server. This is usually represented as `mail.example.com`.|
|MX (Mail Exchange) |TTL|Select the Time to Live (TTL) from the list menu. TTL defaults to 15 minutes.|
|TXT (Text) |Name|Enter the **@** or the **Domain Name**.|
|TXT (Text) |Value|Enter the **record** to verify appropriate email ending rights for a domain or IP.|
|TXT (Text) |TTL|Select the Time to Live (TTL) from the list menu. TTL defaults to 15 minutes.|
|SRV (Service Record) |Service|Enter the **Symbolic Name** of the desired service.|
|SRV (Service Record) |Protocol|Select the **Protocol** being used from the list menu.|
|SRV (Service Record) |Priority|Enter the **Priority** of the target host. The lower the number, the higher the priority.|
|SRV (Service Record) |Weight|Enter the *Relative Weight* for records with the same priority.|
|SRV (Service Record) |Port|Enter the **TCP or UPD Port** on which the service is to be found.|
|SRV (Service Record) |Host (optional)|Enter the **Host Name** for the service.|
|SRV (Service Record) |Target|Enter the **Canonical Host Name** of the machine providing the service.|
|SRV (Service Record) |TTL|Select the Time to Live (TTL) from the list menu. TTL defaults to 15 minutes.|

* Select the **Add Record** button to add the new Zone Record.

### What Happens Next
{:#add-a-dns-zone-record-next}

After adding the Zone Record, it appears in the **Existing Records** section of the screen. You may [edit](#edit-a-dns-zone-record) or [delete](#delete-a-dns-zone-record) the Zone Record at any time.

## Edit a DNS Zone Record
{: #edit-a-dns-zone-record}

Existing DNS Zone Records may be edited by a user to update various areas, such as Time to Live (TTL), Pointer (PTR) records and Host Names. Multiple hosts and aliases may be associated with a DNS Zone Record at any time. Follow the steps below to edit an existing DNS Zone Record.

* Navigate to the desired **DNS Zone** screen by selecting **Classic Infrastructure** from the navigation menu.
* Select **Network > DNS > Forward Zones** from the Classic Infrastructure navigation menu.
* Click on the **row** containing any existing record.

  Records that are italicized cannot be edited. These are generally limited to NS (name server) records.
  {: note}

* Update the details of the record as necessary.
* Select the **Update** button to update the record, or select **Cancel** to cancel the action.

### What Happens Next
{: #edit-a-dns-zone-record-next}

Upon updating the record, its details will display the new entry automatically. Records may be updated at any time, existing records may be deleted, and new records may be [added](#add-a-dns-zone-record).

## Delete a DNS Zone Record
{: #delete-a-dns-zone-record}

Deleting a DNS Zone Record is done through the **DNS Edit Zone** screen. Deleting a DNS Zone Record cannot be undone.
* Select the DNS Zone that has the record you want to delete by clicking the name in the list of DNS Zones.
* Select the Delete icon at then end of the row containing the desired record. A pop-up confirmation box appears.
* Select the **Yes** button to confirm the deletion, or select the **No** button to cancel the action.
