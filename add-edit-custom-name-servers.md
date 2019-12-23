---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Delete Custom Name Servers, Lock Domain Select, Domain Domains

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Add, edit, or delete custom name servers for a domain
{:#add-edit-or-delete-custom-name-servers-for-a-domain}

Domains running on the {{site.data.keyword.BluSoftlayer_notm}} network may point to a maximum of five (5) custom name servers. Custom name servers may be added, deleted or changed by the user at any time. Follow these steps to add, edit, or delete custom name servers for a domain:

1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/){: new_window} and log into your account.
1. From the dashboard, click the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) and select **Classic Infrastructure** to get to the Classic Infrastructure landing page.
1. In the Classic Infrastructure navigation, select **Services > Domain Registration**. 
3. Select the desired **Domain Name** to expand the domain into its snapshot view.
4. Select **Unlocked** from the **Lock Domain**
5. Select the **Add/Edit NS** option in the **Custom Name Servers** section of the screen. A pop-up box will appear.
6. Refer to the table below to complete the appropriate action based on the desired task:
  |Task|Action|
  |:---|:---|
  |Add a custom Name Server|Enter the hostname for the Name Server in the empty field.|
  |Delete a custom Name Server|Delete the information from the field for the appropriate Name Server.|
  |Edit a custom Name Server|Edit the details in the corresponding field for the appropriate Name Server.|

7. Select the **Associate** button to save the changes, or select **Cancel** to cancel the action.

## What happens next
{:#add-edit-or-delete-custom-name-servers-for-a-domain-next}

After you update the name server details, they appear under the **Custom Name Servers** section of the domain. You may update the details at any time.
