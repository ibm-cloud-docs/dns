---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Convert a Secondary DNS Zone to a Primary Zone

At any time, a [Secondary DNS Zone](add-secondary-dns-zone.html){:new_window} may be converted to your Primary zone. When you convert a Secondary DNS Zone to Primary, {{site.data.keyword.BluSoftlayer_notm}} nameservers become the authoritative nameservers for the converted Zone. Follow the steps below to convert a Secondary DNS Zone to Primary:

* Navigate to the **Secondary DNS Zones** screen in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). Refer to [Using the DNS Zones Screen](use-dns-zones-screen.html){:new_window}.
* Select **Convert to Primary** from the **Actions** drop down list for the desired Secondary Zone.
* Select the **Yes** button to convert the Zone, or select **No** to cancel the action.

## What Happens Next

After you convert the Secondary DNS Zone to Primary, you can view it on the **Forward Zones** screen. All SOA and NS records that previously existed for the Zone will be replaced by {{site.data.keyword.BluSoftlayer_notm}} SOA and NS records, which cannot be edited. You may still [edit remaining Zone records](edit-dns-zone-record.html).
