---

copyright:
  years: 2025, 2025
lastupdated: "2025-04-02"

keywords: 

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Updating DNS zones
{: #how-to-update-dns-zones}
{: help}
{: support}

In the DNS interface, you can update **primary zones** and **secondary zones**.
{: shortdesc}

## Updating primary zones
{: #update-dns-primary-zones}

To update primary zones:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](/login) and log in to your account.
1. Click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Infrastructure > Classic Infrastructure**.
1. Select **Network > DNS**.
1. In the Primary zones table, locate the primary zone that you want to update, then click on the name of the zone. 
1. On the zone details page, click the Edit icon ![Edit icon](/images/edit.png) beside the primary zone details you want to edit. In the Records table, locate the Record that you want to edit, then click **Edit** in the Actions menu ![Actions menu](images/overflow.png).


## Updating secondary zones
{: #update-dns-secondary-zones}

You can only edit secondary zone records in your primary provider's interface. 
{: important}

Unlike primary zones, secondary zone records are read-only. You cannot edit secondary zone records in your IBM Cloud account, because the zone is primarily hosted elsewhere. If you want to edit secondary zone records, you must do so on the primary provider. These changes reflect in your IBM Cloud account after the next zone transfer refresh.

If you want your IBM Cloud account to act as a primary provider rather than a secondary provider for your record, see [Converting DNS Zones](/docs/dns?topic=dns-how-to-convert-dns-zones).
