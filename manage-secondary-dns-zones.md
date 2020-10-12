---

copyright:
  years: 1994, 2020
lastupdated: "2020-03-26"

keywords: 

subcollection: dns

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


# Managing secondary DNS zones
{: #manage-secondary-dns-zones}

{{site.data.keyword.cloud}} provides secondary DNS to all customers as a means to cache primary DNS zones in the event of a loss of data. Maintaining a secondary DNS zone is not mandatory, but it is strongly encouraged for users with multiple domains.
{:shortdesc}

Using the DNS Secondary Zones page, you can add, edit, and delete secondary DNS zones. You can also force a transfer to the zone, convert the zone from secondary to primary, and view errors associated with the secondary DNS zone.

To get to the DNS Secondary Zones page:

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: external} and log in to your account.
1. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. From the Classic Infrastructure menu, select **Network > DNS > Secondary Zones** to open the DNS Secondary Zones page.

## Add a secondary DNS zone
{:#add-a-secondary-dns-zone}

Follow these steps to add a secondary DNS zone from the DNS Secondary Zones page:

1. Select the **Add Zone** tab.
1. Enter the domains, IPs (optional), and frequency (optional) in the **Domains** section.
1. Enter the default IP address in the **Default IP** field.
1. Enter the default transfer frequency (in minutes) for which the primary DNS zone will transfer to the secondary DNS zone in the **Default Transfer Frequency** field.
1. Click the **Add Zone** button to add the zone.

## Edit a secondary DNS zone
{:#edit-a-secondary-dns-zone}

Secondary DNS zones can be edited at any time to update the master name server or transfer interval. Follow these steps to edit a secondary DNS zone from the DNS Secondary Zones page:

1. Locate the row pertaining to the zone you want to edit.
1. Click the cells of the row to update the **Master Nameserver** and **Transfer Interval** fields as necessary.
1. Click the **Update** button to update the secondary DNS zone, or select **Cancel** to cancel the action.

## Delete a secondary DNS zone
{:#delete-a-secondary-dns-zone}

A secondary DNS zone can be deleted at any time. Once a secondary DNS zone is deleted, it cannot be recovered. Follow these steps to delete a secondary DNS record from the DNS Secondary Zones page:

1. Locate the row pertaining to the zone you want to delete.
1. Click the **Actions** menu at the end of the row and select **Delete**. A confirmation dialog appears.
1. Click the **Yes** button to confirm the deletion, or click the **No** button to cancel the action.

## Force a zone transfer for a secondary DNS zone
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

In general, DNS zone transfers are automatic, based on the secondary DNS transfer interval specified. If you do not want to wait for the transfer interval, you can force a transfer manually from the DNS Secondary Zones page:

1. Locate the row pertaining to the zone you want to force.
1. Click the **Actions** menu at the end of the row and select **Force Transfer**.

After the transfer begins, the status will change to `Transferring now`. Manual transfers cannot be canceled after they begin. After data is transferred, data transfers return to the transfer interval previously set for the secondary DNS zone. You can update the transfer interval by [editing the secondary DNS zone](#edit-a-secondary-dns-zone) to avoid the need to force the transfer on a frequent basis.

## Convert a secondary DNS zone to a primary zone
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

When you convert a secondary DNS zone to primary, {{site.data.keyword.cloud_notm}} name servers become the authoritative name servers for the converted zone. Follow these steps to convert a secondary DNS zone to primary from the DNS Secondary Zones page:

1. Locate the row pertaining to the zone you want to convert.
1. Click the **Actions** menu at the end of the row and select **Convert to Primary**. A confirmation dialog appears.
1. Click the **Yes** button to convert the zone, or click **No** to cancel the action.

## View errors for a secondary DNS zone
{:#view-error-messages-secondary-dns-zone}

You can view any transfer errors associated with a secondary DNS zone from the DNS Secondary Zones page.

1. Locate the row pertaining to the zone you want to edit.
1. Click the **Actions** menu at the end of the row and select **View Errors**. A dialog appears with the errors.
1. Click the **Close** button to close the errors dialog.
