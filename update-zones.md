---

copyright:
  years: 2025
lastupdated: "2025-04-03"

keywords: 

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Updating DNS zones
{: #how-to-update-dns-zones}
{: help}
{: support}

When updating DNS zones, it's important to understand the difference between primary and secondary zones. Primary zones can be edited directly in your account, while secondary zones are read-only and must be updated through your primary provider's interface. 
{: shortdesc}

## Updating primary zones
{: #update-dns-primary-zones}

To update primary zones:

1. Open the [{{site.data.keyword.cloud_notm}} console](/login) and log in to your account.
1. Click the Navigation Menu icon ![Navigation Menu icon](../icons/icon_hamburger.svg) and select **Infrastructure > Classic Infrastructure**.
1. Select **Network > DNS**.
1. In the Primary zones table, locate the primary zone that you want to update and click its name.
1. On the details page, you can:

   1. Click the Edit icon ![Edit icon](../icons/edit-tagging.svg "Edit") next to the field that you want to update.
   1. Click the Actions icon ![Actions icon](../icons/action-menu-icon.svg) at the end of a row in the Records table to edit or delete a record. 

## Updating secondary zones
{: #update-dns-secondary-zones}

Unlike primary zones, secondary zone records are read-only. You can't edit secondary zone records in your IBM Cloud account because the zone is primarily hosted elsewhere. To update secondary zone records, you must edit these records with the primary provider. Any changes are reflected in your IBM Cloud account after the next zone transfer.

If you'd like your IBM Cloud account to act as a primary provider instead of a secondary provider for your records, see [Converting DNS zones](/docs/dns?topic=dns-how-to-convert-dns-zones).
{: tip}
