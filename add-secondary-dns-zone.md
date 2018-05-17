---
copyright:
  years: 1994, 2017
lastupdated: "2018-05-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Add a Secondary DNS Zone

{{site.data.keyword.BluSoftlayer_notm}} provides Secondary DNS to all customers as a means to cache primary DNS Zones in the event of a loss of data. Maintaining a Secondary DNS Zone is not mandatory, but it is strongly encouraged for users with multiple domains. Follow the steps below to add a Secondary DNS Zone:

* Navigate to the **Secondary DNS Zones** screen in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). Refer to [Using the DNS Zones Screen](use-dns-zones-screen.html){:new_window}.
* Select the **Add Zone** tab.
* Enter the **Domain for the Zone** in the **Zone** field.
* Enter the **Master Name Server's IP Address** in the **Master Nameserver** field.
* Enter the **transfer time** (in minutes) for which the primary DNS Zone will transfer to the Secondary DNS Zone in the **Transfer Interval** field.
* Select the **Add** button to add the Zone, or select **Cancel** to cancel the action.

## What Happens Next

After you create a Secondary DNS Zone, it appears in the list of Zones on the Secondary DNS Zones screen. Transfer of data from the Primary to the Secondary Zone occurs in intervals you specify when the zone is created. At any time, you may [edit](edit-secondary-dns-zone.html), [manually transfer](manual-zone-transfer-secondary-dns.html), or [convert](convert-secondary-dns-primary.html) the Zone to a Primary Zone. The Secondary DNS Zone also may be [deleted](delete-secondary-dns-zone.html) at any time.
