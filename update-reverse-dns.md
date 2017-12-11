---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Update a Reverse DNS Record

Reverse DNS enables users to identify the domain that's associated with an IP address. Customers can update their Reverse DNS records at any time to change the PTR and time to live (TTL). Within the **Manage** version [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/), you can update PTR records in bulk, using the **Search and Replace** tool. This tool allows you to enter a portion of a PTR or the full PTR in the Search field and replace each occurrence within corresponding PTRs with the desired information. 

Please note, this tool works only when existing PTRs are associated with the Server or VLAN. If no PTRs exist, no details are listed and attempts to update will result in an error. 

To add a Reverse DNS PTR record, refer to [Add and Edit a PTR (Pointer) Record](add-and-edit-ptr-pointer-record.html). Follow these steps to update a Reverse DNS record:

 * Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/) using your unique credentials.
 * Select **DNS** from the **Network** drop down menu.
 * Select the **Reverse DNS** menu option.
 * Determine whether the update must be made to all corresponding IP addresses Network VLAN or whether changes will be made to an individual IP.<br><br><table border="1"><tbody><tr><th>If the update will be made to...</th><th>Then...</th></tr><tr><td>Individual IP</td><td><ul><li>Select the <b>drop down menu</b> to see the IP addresses</li><li>Click the desired <strong>IP address</strong> to view the Reverse DNS details associated with the Server.</li></ul></td></tr><tr><td>All corresponding IP addresses on a Network VLAN</td><td><ul><li>Select the <strong> View IP</strong> option after selecting an IP as stated above.</li><li>Select the <strong>Edit RDNS for all IPs in this Subnet</strong> option.</li></ul></td></tr></tbody></table><br/>
 * For individual IPs, just add the **Hostname** and **Reverse TTL** then select **Save**. For the entire **Subnet** highlight the open space under the **Reverse DNS** column and add the **Hostname** the select the **Update** button. This task will need to be done for every IP address in the Subnet.
