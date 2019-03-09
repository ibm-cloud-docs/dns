---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Update DNS Zone Record, edit dns zone record

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Edit a DNS Zone Record
{:#edit-a-dns-zone-record}

Existing DNS Zone Records may be edited by a user to update various areas, such as Time to Live (TTL), Pointer (PTR) records and Host Names. Multiple hosts and aliases may be associated with a DNS Zone Record at any given time. Follow the steps below to edit an existing DNS Zone Record.

* Navigate to the desired **DNS Zone** screen by selecting **Classic Infrastructure** from the navigation menu. 
* Select **Network > DNS > Forward Zones** from the Classic Infrastructure navigation menu.
* Click on the **row** containing any existing record. **Note:** Records that are italicized are not open to edit. This is generally limited to NS (or name server) records.
* Update the details of the record as necessary.
* Select the **Update** button to update the record, or select **Cancel** to cancel the action.

## What Happens Next
{:#edit-a-dns-zone-record-next}

Upon updating the record, its details will automatically display the new entry. Records may be updated at any time, existing records may be deleted, and new records may be [added](/docs/infrastructure/dns?topic=dns-add-a-dns-zone-record).
