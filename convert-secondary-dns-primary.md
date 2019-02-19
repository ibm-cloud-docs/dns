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

# Convert a Secondary DNS Zone to a Primary Zone

At any time, a [Secondary DNS Zone](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window} may be converted to your Primary zone. When you convert a Secondary DNS Zone to Primary, {{site.data.keyword.BluSoftlayer_notm}} nameservers become the authoritative nameservers for the converted Zone. Follow the steps below to convert a Secondary DNS Zone to Primary:

* Navigate to the **Secondary DNS Zones** screen in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/) by selecting **Classic Infrastructure** from the navigation menu. 
* Select **Network > DNS > Secondary Zones** from the Classic Infrastructure navigation menu.
* Select **Convert to Primary** from the **Actions** drop down list for the desired Secondary Zone.
* Select the **Yes** button to convert the Zone, or select **No** to cancel the action.

## What Happens Next

After you convert the Secondary DNS Zone to Primary, you can view it on the **Forward Zones** screen. All SOA and NS records that previously existed for the Zone will be replaced by {{site.data.keyword.BluSoftlayer_notm}} SOA and NS records, which cannot be edited. You may still [edit remaining Zone records](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record).
