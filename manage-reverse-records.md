---

copyright:
  years: 1994, 2025
lastupdated: "2025-04-02"

keywords: 

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# Managing reverse or PTR (pointer) records
{: #manage-reverse-records}

PTR, or pointer, records resolve IP addresses into hostnames. You can add, edit, and delete these records via the **Reverse DNS** feature within each of your public subnets.
{: shortdesc}

To manage reverse DNS records:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/) and log in to your account.
1. From the dashboard, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) and select **Infrastructure > Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Network > IP Management > Subnets**.
1. In the Subnets table, locate the public subnet containing the IP address whose reverse records you want to update, then click on the identifier of the subnet. 
1. On the subnet details page, in the IP addresses table, locate the IP address whose reverse record you want to edit, then click **Edit reverse DNS** in the Actions menu ![Actions menu](images//overflow.png).
1. Complete or update the fields for the record:    
    * **Domain name**: The hostname to which the IP address resolves.
    * **Time to live (TTL)**: The time to live (TTL) for the record.
1. Click **Confirm** to save your changes.

To remove a reverse record, delete all text from the **Domain name** field and click **Confirm**.
{: tip}
