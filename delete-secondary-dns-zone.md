---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Delete a Secondary DNS Zone

After a Secondary DNS Zone has been created, it can be deleted at any time. Be aware that if a Secondary DNS Zone is deleted, it cannot be retrieved. Follow the steps below to delete a Secondary DNS Record.

 * Navigate to the **Secondary DNS Zones** screen in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). Refer to [Using the DNS Zones Screen](use-dns-zones-screen.html){:new_window}.
* Select **Delete** from the **Actions** drop down list for the Zone that requires deletion. A pop-up confirmation box will appear.
  **Note:** If multiple Secondary Zones exist, the view can be filtered to locate the Zone for deletion.
* Select the **Yes** button to confirm the deletion, or select the **No** button to cancel the action.

## What Happens Next

After a Secondary DNS Zone is deleted, the automated transfers from the Primary Zone will cease and the Secondary Zone will no longer exist. If a Secondary DNS Zone is required for the Primary Zone at any time, a new [Secondary DNS Zone may be created](add-secondary-dns-zone.html).
