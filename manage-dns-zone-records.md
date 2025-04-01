---

copyright:
  years: 1994, 2025
lastupdated: "2025-04-01"

keywords:

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Managing DNS zone records
{: #manage-dns-zone-records}

After you [add a DNS zone](/docs/dns?topic=dns-manage-dns-zones#add-a-dns-zone), records can be added to the zone at any time.
{: shortdesc}

To get to the DNS Edit Zone page:

1. From your browser, open the [{{site.data.keyword.cloud}} console](/login){: external} and log in to your account.
1. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. From the Classic Infrastructure menu, select **Network > DNS  > Forward Zones** to open the DNS Forward Zones page.
1. Click the DNS zone to open the DNS Edit Zone page.

## Add a DNS zone record
{: #add-a-dns-zone-record}

The type of records that can be added to a DNS zone include:

* A (Host) Records
* AAAA (Host) Records
* CNAME (Alias) Records
* MX (Mail Exchange) Records
* TXT (Text) Records
* SRV (Service) Records

To add a record to a DNS Zone from the DNS Edit Zone page, select the resource type from the **Resource Type** list, complete the requested fields, and click **Add Record**. Refer to the following table for information on which fields are required for the record type.

| Field | Description |
|-----------|----------|
| Host | Enter the hostname. |
| Points To | Enter the IP address to which the host record points. |
| TTL | Select the Time to Live (TTL) from the list menu. TTL defaults to 15 minutes. |
{: caption="Fields required for A, AAAA, or CNAME records" caption-side="bottom}
{: #a-aaaa-cname-record-fields}
{: tab-title="A, AAAA, CNAME"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| Priority | Enter the priority of the target host. The lower the number, the higher the priority. |
| Host | Enter the hostname. |
| Goes | Enter the `CNAME` of the mail server. For example, `mail.example.com`.|
| TTL | Select the Time to Live (TTL) from the list menu. TTL defaults to 15 minutes.|
{: caption="Fields required for MX records" caption-side="bottom"}
{: #mx-fields}
{: tab-title="MX"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| Name | Enter `@` or the domain name. |
| Value | Enter the record to verify appropriate email ending rights for a domain or IP. |
| TTL | Select the Time to Live (TTL) from the list menu. TTL defaults to 15 minutes. |
{: caption="Fields required for TXT records" caption-side="bottom"}
{: #txt-fields}
{: tab-title="TXT"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| Service | Enter the symbolic name of the service. |
| Protocol | Select the protocol that is being used from the list menu. |
| Priority | Enter the priority of the target host. The lower the number, the higher the priority. |
| Weight | Enter the relative weight for records with the same priority. |
| Port | Enter the TCP or UPD Port on which the service is to be found. |
| Host (optional) | Enter the hostname for the service. |
| Target | Enter the canonical hostname of the machine that provides the service. |
| TTL | Select the Time to Live (TTL) from the list menu. TTL defaults to 15 minutes. |
{: caption="Fields required for SRV records" caption-side="bottom"}
{: #srv-fields}
{: tab-title="SRV"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

## Edit a DNS zone record
{: #edit-a-dns-zone-record}

A user can edit existing DNS zone records to update various areas, such as Time to Live (TTL), Pointer (PTR) records and hostnames. Multiple hosts and aliases can be associated with a DNS zone record at any time. A DNS Zone record can be edited from the DNS Edit Zone page. Click the fields of the record that you want to update. After you update the details of the record, click **Update** to update the record.

Records that are italicized cannot be edited. These records are generally limited to NS (name server) records.
{: note}

## Delete a DNS zone record
{: #delete-a-dns-zone-record}

Deleting a DNS zone record is done through the DNS Edit Zone page. To delete a DNS zone record, click the Delete icon at the end of the row that contains the record. A confirmation dialog appears. Click **Yes** to confirm the deletion or on **No** to cancel the action. Deleting a DNS zone record cannot be undone.
