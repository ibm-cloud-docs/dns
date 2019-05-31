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
* Select the desired **resource type** from the **Resource Type** drop down list.
* Complete the remaining fields for the new Record. Refer to the table below for more information: <br/><br/><table border="1"><tbody><tr><th scope="col">Record Type</th><th scope="col">Field</th><th scope="col">Entry</th></tr><tr><td rowspan="3">A (Host), AAAA (Host) or CNAME (Alias)</td><td>Host</td><td>Enter the <strong>Host Name</strong>.</td></tr><tr><td>Points To</td><td>Enter the <strong>IP Address</strong> to which the Host Record points.</td></tr><tr><td>TTL</td><td>Select the Time to Live (TTL) from the drop down list. TTL defaults to 15 minutes.</td></tr><tr><td rowspan="4">MX (Mail Exchange)</td><td>Priority</td><td>Enter the <strong>Priority</strong> of the target host. The lower the number, the higher the priority.</td></tr><tr><td>Host</td><td>Enter the <strong>Host Name</strong>.</td></tr><tr><td>Goes</td><td>Enter the <strong>CNAME</strong> of the mail server. This is usually represented as `mail.example.com`.</td></tr><tr><td>TTL</td><td>Select the Time to Live (TTL) from the drop down list. TTL defaults to 15 minutes.</td></tr><tr><td rowspan="3">TXT (Text)</td><td>Name</td><td>Enter the <strong>@</strong> or the <strong>Domain Name</strong>.</td></tr><tr><td>Value</td><td>Enter the <strong>record</strong> to verify appropriate email ending rights for a domain or IP.</td></tr><tr><td>TTL</td><td>Select the Time to Live (TTL) from the drop down list. TTL defaults to 15 minutes.</td></tr><tr><td rowspan="8">SRV (Service Record)</td><td>Service</td><td>Enter the <strong>Symbolic Name</strong> of the desired service.</td></tr><tr><td>Protocol</td><td>Select the <strong>Protocol</strong> being used from the drop down list.</td></tr><tr><td>Priority</td><td>Enter the <strong>Priority</strong> of the target host. The lower the number, the higher the priority.</td></tr><tr><td>Weight</td><td>Enter the <strong>Relative Weight</strong> for records with the same priority.</td></tr><tr><td>Port</td><td>Enter the <strong>TCP or UPD Port</strong> on which the service is to be found.</td></tr><tr><td>Host (optional)</td><td>Enter the <strong>Host Name</strong> for the service.</td></tr><tr><td>Target</td><td>Enter the <strong>Canonical Host Name</strong> of the machine providing the service.</td></tr><tr><td>TTL</td><td>Select the Time to Live (TTL) from the drop down list. TTL defaults to 15 minutes.</td></tr></tbody></table><br/>
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
