---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Manage DNS zones
{: #manage-dns-zones}

## Add a DNS Zone
{: #add-a-dns-zone}

DNS management by {{site.data.keyword.cloud}} extends to DNS Zones that may not be on the {{site.data.keyword.cloud_notm}} network. Using our interface, you may add DNS Zones at any time, as a single domain or in bulk. The addition of DNS Zones currently takes place in the [IBM Cloud Console](https://{DomainName}/). Follow the steps below to add one or more DNS Zones.

* Log in to the [IBM Cloud Console](https://{DomainName}/) using your unique credentials.
* Select **Classic Infrastructure** from the Navigation Menu
* Select **DNS** from the **Network** list menu.
* Select **Forward Zones**.
* Select the **Add DNS Zone** tab on the top right.
* Determine whether you are adding a single domain or multiple domains:

### Adding a single Domain
{: #add-single-DomainName}

Complete the following steps in the  **Add single domain** section of the screen:
* Enter the **Domain Name** in the **Domain Name** field.
* Enter the **IP Address** that the domain name will point to in the **IP Address** field.
* Click the **Add Zone** button to add the domain.

### Adding multiple Domains
{: #add-multiple-domains}
Determine if the domains will be associated with a single IP Address or multiple IPs:
* If domains will be associated with a single IP address,
  * Enter **each domain** in the **Domains** text box.
  * Enter the **IP Address** in the **Default IP Address** field.
  * Click the **Add Zone** button to add the domains in bulk.
* If domains will be associated with multiple IP Addresses,
  * Enter **each domain** and its corresponding **IP Address** as a single line item in the **Domains** text box.
  * Click the **Add Zone** button to add the domains in bulk.


### What Happens Next
{:#add-a-dns-zone-next}

After successfully adding a single zone, you are automatically redirected to the Zone Edit page.
New DNS Zones appear in the list of DNS Zones on the [DNS Zones screen](/docs/dns?topic=dns-use-the-dns-zones-screens) within the [IBM Cloud console](https://{DomainName}/). The Zone may be [edited](#edit-a-dns-zone) or [deleted](#delete-a-dns-zone) at any time.

## Edit a DNS Zone
{: edit-a-dns-zone}
Select the DNS Zone you want to edit from the list of zones in the DNS Zones screen by clicking on the name of the zone. This opens the DNS Edit Zone page. From here, you can make changes to the DNS Zone, and click **Update SOA** to commit the changes.

The **Edit a DNS Zone** screen allows you to add new records and edit existing records for the zone you're editing. You may also export or delete the zone from this screen.

### What Happens Next
{:#edit-a-dns-zone-next}

Click **View ALl DNS Zones** to return to the list of DNS Zones.


## Delete a DNS Zone
{: #delete-a-dns-zone}

After a DNS Zone has been added, it may be deleted at any time. DNS Zone deletions are permanent; they cannot be undone. Follow these steps to delete a DNS Zone:

* Navigate to the desired **DNS Zone** screen by selecting **Classic Infrastructure** from the navigation menu.
* Select **Network > DNS** from the Classic Infrastructure navigation menu and choose the type of zone you need.
* Select the **Delete** icon at then end of the row containing the desired DNS Zone. A pop-up confirmation box will appear.
* Select the **Yes** button to confirm the deletion, or select the **No** button to cancel the action.

Zones may also be deleted from within the Edit DNS Zones screen.
{:tip}

### What Happens Next
{:#delete-a-dns-zone-next}

After deleting a DNS Zone, it may no longer be managed using the [IBM Cloud console](https://{DomainName}/). To manage the deleted zone in the Dashboard again, it must be [added as a new Zone](#add-a-dns-zone).
