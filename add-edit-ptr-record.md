---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Add or Edit a PTR (Pointer) Record

PTR, or pointer, records resolve IP addresses into hostnames. Users may add PTR Records to be associated with an IP address by using the Reverse DNS feature on the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/){:new_window}. Also, PTR Records may be edited in the same way they are added. Follow the steps below to add or edit a PTR Record for a device:

* Retrieve the **Public IP Address** for the device that will receive the PTR Record from the **Device List**.
* Display the **Reverse DNS Records** screen** in the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/) by selecting **Classic Infrastructure** from the navigation menu. 
* Select **Network > DNS > Reverse DNS** from the Classic Infrastructure navigation menu.
* Enter the **Public IP Address** retrieved from the Device List in the **View IP** field.
* Click anywhere on the row containing the **Reverse Record** details to open the row for edits.
* Complete or update the fields for the Record based on the table below:<br/><br/><table border="1"><tbody><tr><th>Field</th><th>Entry</th></tr><tr><td>Reverse DNS</td><td>The hostname to which the IP Address will resolve.</td></tr><tr><td>Reverse TTL</td><td>The time to live (TTL) for the new Record</td></tr><tr><td>Notes</td><td>Any applicable notes regarding the Record</td></tr></tbody></table><br/>
* Click the **Update** button to update the record. Click **Cancel** to cancel the action.

## What Happens Next

After a PTR Record is added, the Public IP Address associated with that record will resolve to the hostname specified in the record. The record may be edited at any time. To remove details from the PTR Record, delete all information from the fields using the **Edit** process.
