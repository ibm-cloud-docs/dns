---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Manual Zone Transfer, DNS Zone transfers, Secondary DNS Zone

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# Make a Manual Zone Transfer for a Secondary DNS Zone
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

In general, DNS Zone transfers are completed automatically, based on the Secondary DNS transfer interval you've specified. You can use a Manual Zone transfer to force content to transfer that would otherwise wait until the next automatic transfer. To complete a manual transfer, a [Secondary DNS Zone must be established](/docs/dns?topic=dns-add-a-secondary-dns-zone). Follow the steps in this article to make a Manual Zone transfer for a Secondary DNS.

1. Navigate to the **Secondary DNS Zones** screen in the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/). Refer to [Using the DNS Zones Screen](/docs/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window}.
2. Select **Force Transfer** from the **Actions** list to begin the transfer.

## What Happens Next
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone-next}

After the transfer begins, the Status will change to **Transferring now**. Manual transfers may not be canceled after they begin. After data has been transferred, data transfers will return to the transfer interval previously set for the Secondary DNS. The [transfer interval may be changed](/docs/dns?topic=dns-edit-a-secondary-dns-zone) at any time to avoid the need to make manual Zone transfers on a frequent basis.
