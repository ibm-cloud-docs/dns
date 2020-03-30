---

copyright:
  years: 1994, 2020
lastupdated: "2020-03-26"

keywords: transfer domain, transfer existing domain, transfer multiple domains

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:external: target="_blank" .external}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Transferring an existing domain
{: #transfer-domains}
{: help}
{: support}

After a domain has been registered, it can be transferred at any time. Transferring a domain from a third-party registrar to {{site.data.keyword.cloud}} can streamline the domain management process. Transferring a domain does not affect the website, email, or DNS. It only changes the registrar that manages the domain records. Follow these steps to transfer an existing domain to {{site.data.keyword.cloud_notm}}.

## Transfer a single domain
{: #transfer-single-domain}

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: external} and log in to your account.
1. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. From the Classic Infrastructure menu, select **Services > Domain Registration** to open the Domains page.
1. Choose the **Transfer** tab.
1. Enter the existing domain name in the **Domain Name** field.
1. Select the domain type from the **Domain Type** list.
1. Select the amount of time for which the domain will remain active from the **Registration Time** list.

  The price for each time period is displayed next to the amount of time and will be charged to the account when the new domain is transferred.
  {:note}

1. Click the **Continue** button to transfer the domain.

## Transfer multiple domains
{: #transfer-multiple-domains}

Domains can be transferred to {{site.data.keyword.cloud_notm}} in bulk as well. Follow these steps to transfer multiple domains.

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: external} and log in to your account.
1. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. From the Classic Infrastructure menu, select **Services > Domain Registration** to open the Domains page.
1. Choose the **Transfer** tab.
1. Select the **Transfer Multiple Domains?** option within the **Transfer** tab.
1. Enter the existing domain name in the **Domain Name** field.
1. Select the domain type from the **Domain Type** list.
1. Select the amount of time for which the transferred domain remains active from the **Registration Time** list.

   The price for each time period is displayed next to the amount of time and will be charged to the account when the new domain is transferred.
   {:note}

1. Repeat for each additional domain to be transferred.

   Select the **Add Another** option to populate additional blank fields for more domain entries. Select the **Delete** icon to delete an entire entry from the page.
   {:note}

1. Click the **Continue** button to transfer the domains.

## Next steps
{:#transfer-an-existing-domain-to-ibm-cloud-next}

After you transfer a domain, you can use the [DNS interface](/docs/dns?topic=dns-how-to-use-the-dns-interface) to manage it. When the domain's registration approaches its expiration date, you can [renew the domain](/docs/dns?topic=dns-renew-an-existing-domain).
