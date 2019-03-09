---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Delete a Secondary DNS Zone
{:#delete-a-secondary-dns-zone}

After a Secondary DNS Zone has been created, it can be deleted at any time. Be aware that if a Secondary DNS Zone is deleted, it cannot be retrieved. Follow the steps below to delete a Secondary DNS Record.

 * Navigate to the **Secondary DNS Zones** screen in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/) by selecting **Classic Infrastructure** from the navigation menu. 
* Select **Network > DNS > Secondary Zones** from the Classic Infrastructure navigation menu.
* Select **Delete** from the **Actions** drop down list for the Zone that requires deletion. A pop-up confirmation box will appear.
  If multiple Secondary Zones exist, the view can be filtered to locate the Zone for deletion.
  {:note}
* Select the **Yes** button to confirm the deletion, or select the **No** button to cancel the action.

## What Happens Next
{:#delete-a-secondary-dns-zone-next}

After a Secondary DNS Zone is deleted, the automated transfers from the Primary Zone will cease and the Secondary Zone will no longer exist. If a Secondary DNS Zone is required for the Primary Zone at any time, a new [Secondary DNS Zone may be created](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone).
