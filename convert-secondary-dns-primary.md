---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Convert a Secondary DNS Zone to a Primary Zone
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

At any time, a [Secondary DNS Zone](/docs/dns?topic=dns-add-a-secondary-dns-zone){:new_window} may be converted to your Primary zone. When you convert a Secondary DNS Zone to Primary, {{site.data.keyword.cloud_notm}} name servers become the authoritative name servers for the converted Zone. Follow the steps below to convert a Secondary DNS Zone to Primary:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > DNS > Secondary Zones**.
1. Select **Convert to Primary** from the **Actions** list for the desired Secondary Zone.
1. Select the **Yes** button to convert the Zone, or select **No** to cancel the action.

## What Happens Next
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

After you convert the Secondary DNS Zone to Primary, you can view it on the **Forward Zones** screen. All SOA and NS records that previously existed for the Zone will be replaced by {{site.data.keyword.cloud_notm}} SOA and NS records, which cannot be edited. You may still [edit remaining Zone records](/docs/dns?topic=dns-edit-a-dns-zone-record).
