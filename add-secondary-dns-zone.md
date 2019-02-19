---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Add a Secondary DNS Zone

{{site.data.keyword.BluSoftlayer_notm}} provides Secondary DNS to all customers as a means to cache primary DNS Zones in the event of a loss of data. Maintaining a Secondary DNS Zone is not mandatory, but it is strongly encouraged for users with multiple domains. Follow the steps below to add a Secondary DNS Zone:

* Navigate to the **Secondary DNS Zones** screen in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/) by selecting **Classic Infrastructure** from the navigation menu. 
* Select **Network > DNS > Secondary Zones** from the Classic Infrastructure navigation menu.
* Select the **Add Zone** tab.
* Enter the **Domain for the Zone** in the **Zone** field.
* Enter the **Master Name Server's IP Address** in the **Master Nameserver** field.
* Enter the **transfer time** (in minutes) for which the primary DNS Zone will transfer to the Secondary DNS Zone in the **Transfer Interval** field.
* Select the **Add** button to add the Zone, or select **Cancel** to cancel the action.

## What Happens Next

After you create a Secondary DNS Zone, it appears in the list of Zones on the Secondary DNS Zones screen. Transfer of data from the Primary to the Secondary Zone occurs in intervals you specify when the zone is created. At any time, you may [edit](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record), [manually transfer](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone), or [convert](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone) the Zone to a Primary Zone. The Secondary DNS Zone also may be [deleted](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone) at any time.
