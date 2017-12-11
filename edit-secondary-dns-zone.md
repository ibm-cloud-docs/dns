---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Edit a Secondary DNS Zone

Secondary DNS Zones may be edited at any time to update the Master Nameserver or Transfer Interval. Follow the steps below to edit a Secondary DNS Zone.

* Navigate to the **Secondary DNS Zones** screen in the Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). Refer to [Using the DNS Zones Screen](delete-secondary-dns-record.html){:new_window}.
* Click anywhere on the **row containing the Secondary DNS Zone** to open the Zone for edits.
  * **Note:** If multiple Secondary Zones exist, the view can be filtered to locate the Zone requiring edits.
* Update the **Master Nameserver** and **Transfer Interval** fields as necessary.
* Select the **Update** button to update the Secondary DNS Zone, or select **Cancel** to cancel the action.

## What Happens Next

After editing the Secondary DNS Zone, the **Master Nameserver** and **Transfer Interval** values will reflect the update and the Secondary Zone will begin receiving transfers based on the new information. At any time, the Zone may be edited again by repeating the steps above.
