---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
# Update a Reverse DNS Record

Reverse DNS enables users to identify the domain that's associated with an IP address. Customers can update their Reverse DNS records at any time to change the PTR and time to live (TTL). Within the **Manage** version [IBM Cloud Console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/), you can update PTR records in bulk, using the **Search and Replace** tool. This tool allows you to enter a portion of a PTR or the full PTR in the Search field and replace each occurrence within corresponding PTRs with the desired information. 

Please note, this tool works only when existing PTRs are associated with the Server or VLAN. If no PTRs exist, no details are listed and attempts to update will result in an error. 

To add a Reverse DNS PTR record, refer to [Add and Edit a PTR (Pointer) Record](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record). Follow these steps to update a Reverse DNS record:

 * Navigate to the [IBM Cloud Console ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/) using your unique credentials.
 * Select **Classic Infrastructure** from the navigation menu.
 * Select **Network > DNS > Reverse DNS** from the Classic Infrastructure navigation menu.
 * Type in the IP address, or select it from the drop down menu and click **View IP**.
 * Edit the options listed and click **Save**. You can also choose **Edit RDNS for all IPs in this Subnet** to make changes across the entire subnet. 
 

