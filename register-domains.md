---

copyright:
  years: 1994, 2023
lastupdated: "2023-06-08"

keywords:

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Registering new domains
{: #register-a-new-domain}
{: help}
{: support}

Effective 30 June 2023, IBM Cloud will no longer support the Domain Name Registration service, which is offered in partnership with Tucows Inc. For more information, see [Domain Name Registration domain transfer](/docs/dns?topic=dns-domain-name-registration-domain-transfer).
{: deprecated}

Follow these steps to register a new domain, either one at a time, or multiple domains at one time.
{: shortdesc}

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: external} and log in to your account.
1. Select the Menu icon ![Menu icon](../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. From the Classic Infrastructure menu, select **Services > Domain Registration** to open the Domains page.
1. Choose the **Register** tab.

   Select the **Register Multiple Domains?** option within the **Register** tab if you are registering multiple domains at one time.
   {: tip}

1. Enter the new domain name in the **Domain Name** field.
1. Select the domain type from the **Domain** list.
1. Select the amount of time to reserve the domain from the **Registration Time** list.

    The price for each time period is displayed next to the amount of time and is charged to the account when the new domain is registered.
    {: note}

1. If you register multiple domains, select the **Add Another** option to populate more blank fields for more domain entries.

   Select the **Delete** icon to delete an entire entry from the page.
   {: note}

1. Click **Check Availability** to check whether the domain names are available. If all domains are available, proceed to the next step. If one or more domains are not available, try again with another domain.
1. Click **Continue** to register the domain.

## Next steps
{: #register-a-new-domain-next}

After you register a domain, you can use the [DNS interface](/docs/dns?topic=dns-how-to-use-the-dns-interface) to manage it. When the domain's registration approaches its expiration date, you can [renew the domain](/docs/dns?topic=dns-renew-an-existing-domain).
