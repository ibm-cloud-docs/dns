---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Add a DNS Zone

DNS management by {{site.data.keyword.BluSoftlayer_notm}} extends to DNS Zones that may not be on the {{site.data.keyword.BluSoftlayer_notm}} network. Using our interface, you may add DNS Zones at any time, as a single domain or in bulk. The addition of DNS Zones currently takes place in the [Control](https://control.softlayer.com/) version of the Customer Portal. Follow the steps below to add one or more DNS Zones

* Log in to the [Control](https://control.softlayer.com/) version of the Customer Portal using your unique credentials.
* Select **DNS** from the **Network** drop down menu.
* Select **Forward Zones**.
* Select the **Add DNS Zone** tab on the top right.
* Determine whether you are adding a single domain or multiple domains:<br> <br><table border="1"><tbody><tr><th>If adding...</th><th>Then...</th></tr><tr><td>A single domain</td><td>Complete he following steps in the <strong>Add single domain</strong> section of the screen:<br> <ul><li>Enter the <strong>Domain Name</strong> in the <strong>Domain Name</strong> field.</li><li>Enter the <strong>IP Address</strong> that the domain name will point to in the <strong>IP Address</strong> field.</li><li>Click the <strong>Add Zone</strong> button to add the domain.<br> </li></ul></td></tr><tr><td>Multiple Domains</td><td>Determine if the domains will be associated with a single IP Address or multiple IPs:<br> <p> </p><p> </p><p> </p><p> </p><ul><li>If domains will be associated with a single IP address,<ul><li>Enter <strong>each domain</strong> in the <strong>Domains</strong> text box.</li><li>Enter the <strong>IP Address</strong> in the <strong>Default IP Address</strong> field.</li><li>Click the <strong>Add Zone</strong> button to add the domains in bulk.</li></ul></li><li>If domains will be associated with multiple IP Addresses,<ul><li>Enter <strong>each domain</strong> and its corresponding <strong>IP Address</strong> as a single line item in the <strong>Domains</strong> text box.</li><li>Click the <strong>Add Zone</strong> button to add the domains in bulk.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## What Happens Next

After adding a DNS Zone, it appears in the list of DNS Zones on the [DNS Zones screen](access-dns-zones-screen.html) within the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). The Zone may be [edited](edit-dns-zone-record.html) or [deleted](delete-dns-zone.html) at any time.
