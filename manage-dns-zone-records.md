---

copyright:
  years: 1994, 2025
lastupdated: "2025-04-02"

keywords:

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Managing DNS zone records
{: #manage-dns-zone-records}

After you [create a DNS zone](/docs/dns?topic=dns-how-to-create-dns-zones), you can add records to the zone at any time. You can add, edit, or delete primary zone records in your account. 
{: shortdesc}

You can only edit secondary zone records in your primary provider's interface. 
{: important}

Unlike primary zones, secondary zone records are read-only. You cannot edit secondary zone records in your IBM Cloud account, because the zone is primarily hosted elsewhere. If you want to edit secondary zone records, you must do so on the primary provider. These changes reflect in your IBM Cloud account after the next zone transfer refresh.

If you want your IBM Cloud account to act as a primary provider rather than a secondary provider for your record, see [Converting DNS Zones](/docs/dns?topic=dns-how-to-convert-dns-zones).

## Addding a DNS zone record
{: #add-a-dns-zone-record}

The type of records that you can add to a DNS zone include:

* A (Host) Records
* AAAA (Host) Records
* CNAME (Alias) Records
* MX (Mail Exchange) Records
* NS (Name Server) Records
* SRV (Service) Records
* TXT (Text) Records

To add a Primary zone record to a DNS Zone:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](/login) and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS**.
1. In the Primary zones table, locate the primary zone that you want to update, then click on the name of the zone.
1. On the Primary zone details page, click **Create** in the Records table. 
1. Enter a name for your record, select a record type, and complete the other requested fields, athen click **Create**.

Refer to the following tables for information on which fields are required for the record type.
{: note}

### Fields required for A, AAAA, CNAME, MX, NS, SRV, or TXT records
{: #fields-required-dns-records}

| Field | Description |
|-----------|----------|
| IPv4 address | Enter an IPv4 address.|
{: caption="Fields required for A records" caption-side="bottom"}
{: #a-fields}
{: tab-title="A"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| IPv6 address | Enter an IPv6 address.|
{: caption="Fields required for AAAA records" caption-side="bottom"}
{: #aaaa-fields}
{: tab-title="AAAA"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| Target hostname | Enter the target hostname.|
{: caption="Fields required for CNAME records" caption-side="bottom"}
{: #cname-fields}
{: tab-title="CNAME"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| Mail server hostname | Enter the hostname. |
| Priority | Enter the priority of the target host. The lower the number, the higher the priority. |
{: caption="Fields required for MX records" caption-side="bottom"}
{: #mx-fields}
{: tab-title="MX"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| Name server hostname | Enter `@` or the domain name. |
{: caption="Fields required for NS records" caption-side="bottom"}
{: #ns-fields}
{: tab-title="NS"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| Target hostname and port | Enter the canonical hostname of the machine that provides the service, enter a semicolon, then enter the TCP or UPD Port on which the service is to be found. |
| Weight | Enter the relative weight for records with the same priority. |
| Priority | Enter the priority of the target host. The lower the number, the higher the priority. |
{: caption="Fields required for SRV records" caption-side="bottom"}
{: #srv-fields}
{: tab-title="SRV"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

| Field | Description |
|-----------|----------|
| Data | Enter the data in parentheses. |
{: caption="Fields required for TXT records" caption-side="bottom"}
{: #txt-fields}
{: tab-title="TXT"}
{: tab-group="recordfields"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the fields required and their description."}

## Editing a DNS zone record
{: #edit-a-dns-zone-record}

You can edit existing DNS zone records to update various areas, such as name, record type, and hostnames. Multiple hosts and aliases can be associated with a DNS zone record at any time.

To edit a Primary zone record:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](/login) and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS**.
1. In the Primary zones table, locate the primary zone that you want to update, then click on the name of the zone.
1. On the Primary zone details page, locate the Record that you want to edit in the Records table, then click **Edit** in the Actions menu ![Actions menu](images/actions-icon-vertical.svg).
1. Update the name, type, hostname, and other details of the record.
2. Click **Update** to update the record.

## Deleting a DNS zone record
{: #delete-a-dns-zone-record}

You can delete a DNS zone record through the DNS Zone details page. 

To delete a Primary zone record:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](/login) and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS**.
1. In the Primary zones table, locate the primary zone that you want to update, then click on the name of the zone.
1. On the Primary zone details page, locate the Record that you want to edit in the Records table, then click **Delete** in the Actions menu ![Actions menu](images/actions-icon-vertical.svg).
1. Click **Confirm** to delete the record.
