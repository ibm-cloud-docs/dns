---

copyright:
  years: 1994, 2020
lastupdated: "2020-03-26"

keywords: 

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Managing DNS zones
{: #manage-dns-zones}

DNS management by {{site.data.keyword.cloud}} extends to DNS zones that might not be on the {{site.data.keyword.cloud_notm}} network. Using the DNS Forward Zones page, you can add, edit, and delete DNS zones.
{: shortdesc}

To get to the DNS Forward Zones page:

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: external} and log in to your account.
1. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. From the Classic Infrastructure menu, select **Network > DNS  > Forward Zones** to open the DNS Forward Zones page.

## Add a DNS zone
{: #add-a-dns-zone}

Follow these steps to add a DNS zone in the DNS Forward Zones page:

1. Select the **Add DNS Zone** tab.
1. Enter the domains and IPs (optional) in the **Domains** field.
1. Enter the default IP address in the **Default IP** field.
1. Click the **Add Zone** button to add the DNS zone.

After you added the DNS zone, you can [add records](/docs/dns?topic=dns-manage-dns-zone-records#add-a-dns-zone-record) to the zone.

## Edit a DNS zone
{: #edit-a-dns-zone}

Select the DNS zone you want to edit from the list of zones in the DNS Forward Zones page by clicking on the name of the zone. This opens the DNS Edit Zone page. From here, you can make changes to the DNS zone, and click **Update SOA** to commit the changes.

The **DNS Edit Zone** page allows you to add new records and edit existing records for the zone. You can also export or delete the zone from this page.


## Delete a DNS zone
{: #delete-a-dns-zone}

After a DNS zone is added, it can be deleted at any time. DNS zone deletions are permanent; they cannot be undone. Follow these steps to delete a DNS zone in the DNS Forward Zones page:

1. Select the **Delete** icon at the end of the row containing the DNS zone. A confirmation dialog appears.
1. Click the **Yes** button to confirm the deletion, or click the **No** button to cancel the action.

Zones can also be deleted from within the Edit DNS Zones page.
{: tip}
