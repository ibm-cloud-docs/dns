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

1. From your browser, open the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/){: new_window} and log into your account.
2. In the Customer Portal navigation, select **Classic Infrastructure** from the navigation menu.
1. Select **Services > Domain Registration** from the Classic Infrastructure navigation menu.
3. Select the desired **Domain Name** to expand the domain into its snapshot view.
4. Select **Unlocked** from the **Lock Domain**
5. Select the **Add/Edit NS** option in the **Custom Name Servers** section of the screen. A pop-up box will appear.
6. Refer to the table below to complete the appropriate action based on the desired task:<br/><br/><table border="1"><tbody><tr><th>Task</th><th>Action</th></tr><tr><td>Add a custom Name Server</td><td>Enter the hostname for the Name Server in the empty field.</td></tr><tr><td>Delete a custom Name Server</td><td>Delete the information from the field for the appropriate Name Server.</td></tr><tr><td>Edit a custom Name Server</td><td>Edit the details in the corresponding field for the appropriate Name Server.</td></tr></tbody></table>
7. Select the **Associate** button to save the changes, or select **Cancel** to cancel the action.

## What happens next
{:#add-edit-or-delete-custom-name-servers-for-a-domain-next}

After you update the name server details, they appear under the **Custom Name Servers** section of the domain. You may update the details at any time.
