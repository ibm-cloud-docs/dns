---

copyright:
  years: 1994, 2020
lastupdated: "2020-03-26"

keywords: 

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Managing reverse or PTR (Pointer) records
{:#add-or-edit-a-ptr-pointer-record}

PTR, or pointer, records resolve IP addresses into hostnames. Users can add PTR records to be associated with an IP address by using **Reverse Records**. Also, PTR records can be edited in the same way they are added. Follow these steps to add or edit a PTR record for a device.
{:shortdesc}

Have the **public IP address** for the device that will receive the PTR record ready.
{: important}

1. From your browser, open the [{{site.data.keyword.cloud}} console](https://{DomainName}/){: external} and log in to your account.
1. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. From the Classic Infrastructure menu, select **Network > DNS  > Reverse Records** to open the Reverse DNS Records page.
1. Enter the public IP address of the device in the **View IP** field.
1. Complete or update the fields for the record based on the following:    
    * **Hostname**: The hostname to which the IP address resolves.
    * **Reverse TTL**: The time to live (TTL) for the new record.
1. Click the **Save** button to save the record.

You can also choose **Edit RDNS for all IPs in this Subnet** to make changes across the entire subnet. To remove details from the PTR record, delete all information from the fields and click the **Save** button.
