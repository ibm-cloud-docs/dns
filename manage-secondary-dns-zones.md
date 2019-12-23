---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

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


# Manage Secondary DNS zones
{: #manage-secondary-dns-zones}

{{site.data.keyword.cloud}} provides Secondary DNS to all customers as a means to cache primary DNS Zones in the event of a loss of data. Maintaining a Secondary DNS Zone is not mandatory, but it is strongly encouraged for users with multiple domains.


## Add a Secondary DNS Zone
{:#add-a-secondary-dns-zone}

Follow the steps below to add a Secondary DNS Zone:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Secondary Zones**.
1. Select the **Add Zone** tab.
1. Enter the **Domain for the Zone** in the **Zone** field.
1. Enter the **Master Name Server's IP Address** in the **Master name server** field.
1. Enter the **transfer time** (in minutes) for which the primary DNS Zone will transfer to the Secondary DNS Zone in the **Transfer Interval** field.
1. Select the **Add** button to add the Zone, or select **Cancel** to cancel the action.

### What happens after adding
{:#add-a-secondary-dns-zone-next}

After you create a Secondary DNS Zone, it appears in the list of Zones on the Secondary DNS Zones screen. Transfer of data from the Primary to the Secondary Zone occurs in intervals you specify when the zone is created. At any time, you may [edit](#edit-a-secondary-dns-zone), [manually transfer](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone), or [convert](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) the Zone to a Primary Zone. The Secondary DNS Zone also may be [deleted](#delete-a-secondary-dns-zone) at any time.

## Edit a Secondary DNS Zone
{:#edit-a-secondary-dns-zone}

Secondary DNS Zones may be edited at any time to update the master name server or Transfer Interval. Follow the steps below to edit a Secondary DNS Zone.

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Secondary Zones**.
1. Click anywhere on the **row containing the Secondary DNS Zone** to open the Zone for edits.
  If multiple Secondary Zones exist, the view can be filtered to locate the Zone requiring edits.
  {:note}  
1. Update the **Master name server** and **Transfer Interval** fields as necessary.
1. Select the **Update** button to update the Secondary DNS Zone, or select **Cancel** to cancel the action.

### What happens after editing
{:#edit-a-secondary-dns-zone-next}

After editing the Secondary DNS Zone, the **Master name server** and **Transfer Interval** values will reflect the update and the Secondary Zone will begin receiving transfers based on the new information. At any time, the Zone may be edited again by repeating the previous steps.

## Delete a Secondary DNS Zone
{:#delete-a-secondary-dns-zone}

After a Secondary DNS Zone has been created, it can be deleted at any time. Be aware that if a Secondary DNS Zone is deleted, it cannot be retrieved. Follow these steps to delete a Secondary DNS Record.

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Secondary Zones**.
1. Select **Delete** from the **Actions** list menu for the Zone that requires deletion. A pop-up confirmation box will appear.
  If multiple Secondary Zones exist, the view can be filtered to locate the Zone for deletion.
  {:note}
1. Select the **Yes** button to confirm the deletion, or select the **No** button to cancel the action.

### What happens after deleting
{:#delete-a-secondary-dns-zone-next}

After a Secondary DNS Zone is deleted, the automated transfers from the Primary Zone will cease and the Secondary Zone will no longer exist. If a Secondary DNS Zone is required for the Primary Zone at any time, a new [Secondary DNS Zone may be created](#add-a-secondary-dns-zone).
