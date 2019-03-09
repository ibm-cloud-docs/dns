---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Master Nameserver

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Edit a Secondary DNS Zone
{:#edit-a-secondary-dns-zone}

Secondary DNS Zones may be edited at any time to update the Master Nameserver or Transfer Interval. Follow the steps below to edit a Secondary DNS Zone.

* Navigate to the **Secondary DNS Zones** screen in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/) by selecting **Classic Infrastructure** from the navigation menu. 
* Select **Network > DNS > Secondary Zones** from the Classic Infrastructure navigation menu.
* Click anywhere on the **row containing the Secondary DNS Zone** to open the Zone for edits.
  If multiple Secondary Zones exist, the view can be filtered to locate the Zone requiring edits.
  {:note}  
* Update the **Master Nameserver** and **Transfer Interval** fields as necessary.
* Select the **Update** button to update the Secondary DNS Zone, or select **Cancel** to cancel the action.

## What Happens Next
{:#edit-a-secondary-dns-zone-next}

After editing the Secondary DNS Zone, the **Master Nameserver** and **Transfer Interval** values will reflect the update and the Secondary Zone will begin receiving transfers based on the new information. At any time, the Zone may be edited again by repeating the steps above.
