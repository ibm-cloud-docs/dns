---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Make a Manual Zone Transfer for a Secondary DNS Zone

In general, DNS Zone transfers are completed automatically, based on the Secondary DNS transfer interval you've specified. You can use a Manual Zone transfer to force content to transfer that would otherwise wait until the next automatic transfer. To complete a manual transfer, a [Secondary DNS Zone must be established](add-secondary-dns-zone.html). Follow the steps in this article to make a Manual Zone transfer for a Secondary DNS.

1. Navigate to the **Secondary DNS Zones** screen in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). Refer to [Using the DNS Zones Screen](delete-secondary-dns-record.html){:new_window}.
2. Select **Force Transfer** from the **Actions** drop-down list to begin the transfer.

## What Happens Next

After the transfer begins, the Status will change to **Transferring now**. Manual transfers may not be canceled after they begin. After data has been transferred, data transfers will return to the transfer interval previously set for the Secondary DNS. The [transfer interval may be changed](edit-secondary-dns-zone.html) at any time to avoid the need to make manual Zone transfers on a frequent basis.
