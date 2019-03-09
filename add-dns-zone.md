---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone, DNS management, Add DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Add a DNS Zone
{:#add-a-dns-zone}

DNS management by {{site.data.keyword.BluSoftlayer_notm}} extends to DNS Zones that may not be on the {{site.data.keyword.BluSoftlayer_notm}} network. Using our interface, you may add DNS Zones at any time, as a single domain or in bulk. The addition of DNS Zones currently takes place in the [Control](https://control.softlayer.com/) version of the Customer Portal. Follow the steps below to add one or more DNS Zones

* Log in to the [Control](https://control.softlayer.com/) version of the Customer Portal using your unique credentials.
* Select **Classic Infrastructure** from the Navigation Menu
* Select **DNS** from the **Network** drop down menu.
* Select **Forward Zones**.
* Select the **Add DNS Zone** tab on the top right.
* Determine whether you are adding a single domain or multiple domains:<br> <br><table border="1"><tbody><tr><th>If adding...</th><th>Then...</th></tr><tr><td>A single domain</td><td>Complete the following steps in the <strong>Add single domain</strong> section of the screen:<br> <ul><li>Enter the <strong>Domain Name</strong> in the <strong>Domain Name</strong> field.</li><li>Enter the <strong>IP Address</strong> that the domain name will point to in the <strong>IP Address</strong> field.</li><li>Click the <strong>Add Zone</strong> button to add the domain.<br> </li></ul></td></tr><tr><td>Multiple Domains</td><td>Determine if the domains will be associated with a single IP Address or multiple IPs:<br> <p> </p><p> </p><p> </p><p> </p><ul><li>If domains will be associated with a single IP address,<ul><li>Enter <strong>each domain</strong> in the <strong>Domains</strong> text box.</li><li>Enter the <strong>IP Address</strong> in the <strong>Default IP Address</strong> field.</li><li>Click the <strong>Add Zone</strong> button to add the domains in bulk.</li></ul></li><li>If domains will be associated with multiple IP Addresses,<ul><li>Enter <strong>each domain</strong> and its corresponding <strong>IP Address</strong> as a single line item in the <strong>Domains</strong> text box.</li><li>Click the <strong>Add Zone</strong> button to add the domains in bulk.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## What Happens Next
{:#add-a-dns-zone-next}

After adding a DNS Zone, it appears in the list of DNS Zones on the [DNS Zones screen](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) within the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/). The Zone may be [edited](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record) or [deleted](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone) at any time.


