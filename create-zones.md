---

copyright:
  years: 2025, 2025
lastupdated: "2025-05-08"

keywords: 

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Creating DNS zones
{: #how-to-create-dns-zones}
{: help}
{: support}

In the DNS interface, you can create **primary zones** and **secondary zones**. When creating DNS zones, it's important to understand the difference between primary and secondary zones. Primary zones can be created and edited directly in your account, while secondary zones are read-only and must be imported from and updated through your primary provider's interface.
{: shortdesc}

## Creating primary zones
{: #create-dns-primary-zones}

To create primary zones:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](/login) and log in to your account.
1. Click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Infrastructure > Classic Infrastructure**.
1. Select **Network > DNS**.
1. In the Primary zones table, click **Create**.
1. Enter a name for your primary zone, then click **Confirm.**

## Creating secondary zones
{: #create-dns-secondary-zones}

To create secondary zones:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](/login) and log in to your account.
1. Click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Infrastructure > Classic Infrastructure**.
1. Select **Network > DNS**.
1. In the Secondary zones table, click **Create**.
1. Enter a name, enter a primary name server, and select a transfer interval for your secondary zone, then click **Confirm**.
