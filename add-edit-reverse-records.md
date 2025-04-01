---

copyright:
  years: 1994, 2025
lastupdated: "2025-04-01"

keywords: 

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Add or edit reverse or PTR (Pointer) records
{: #add-or-edit-reverse-records}

PTR, or pointer, records resolve IP addresses into hostnames. Users can add PTR records to be associated with an IP address by using **Reverse Records**. Also, PTR records can be edited in the same way they are added. Follow these steps to add or edit a PTR record for a device.
{: shortdesc}

Have the **public IP address** for the device that receives the PTR record ready.
{: important}

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/) and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Infrastructure > Classic Infrastructure**.
1. Select **Network > IP Management > Subnets**.
1. Click the subnet link to view the subnet's details.
1. On the the **Subnet Details** page, select the **Reserved IPs** tab.
1. Select **Edit reverse DNS** from the overflow menu ![overflow menu](images/overflow.png).
1. Enter the Reverse DNS in the field provided.
1. Select a Reverse TTL from the list.
1. Complete or update the fields for the record:    
    * **Hostname**: The hostname to which the IP address resolves.
    * **Reverse TTL**: The time to live (TTL) for the new record.
1. Click **Update** to save your changes.

You can also choose **Edit RDNS for all IPs in this Subnet** so that you can make changes across the entire subnet. To remove details from the PTR record, delete all information from the fields and click **Save**.
