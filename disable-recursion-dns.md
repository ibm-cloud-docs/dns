---

copyright:
  years: 1994, 2020
lastupdated: "2020-03-26"

keywords:

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Disabling recursion for DNS
{: #disable-recursion-for-dns}

{{site.data.keyword.cloud}} DNS servers perform recursion by default. Recursion allows your DNS server to contact other DNS servers to assist in resolving domain names when it cannot resolve the domain itself. Recursion can prove to be useful when necessary; however, it also opens the DNS server open to attack, which could take down the DNS server altogether. System administrators generally identify a need for recursion and act accordingly. Otherwise, it is best to disable recursion. Follow these steps based on your operating system or control panel to disable DNS recursion.
{: shortdesc}

## Disable recursion in Plesk
{: #disable-recursion-in-plesk}

1. Log in to the **Plesk Admin Panel**.
1. Select **Tools and Settings**.
1. Click **DNS Template Settings** from the section.
1. Select **Localnets** from the **DNS Recursion** section.
1. Click the **OK** button.

## Disable recursion in Windows Server 2003 and 2008
{: #disable-recursion-in-windows-server}

1. Open **DNS Manager** from the **Start** menu by clicking **Start > Administrative Tools > DNS**.
1. Right-click on the **DNS Server** in the **Console Tree**.
1. Select the **Properties** tab.
1. Click the **Advanced** button in the **Server Options** section.
1. Select the **Disable Recursion** checkbox.
1. Click the **OK** button.

## Disable recursion in Linux
{: #disable-recursion-in-linux}

1. Locate the BIND configuration file within the operating system. The BIND configuration file is usually located in one of the following paths:
   * `/etc/bind/named.conf`
   * `/etc/named.conf`

1. Open the `named.conf` file in your preferred editor.
1.  Add the following parameters to the **Options** section:

    * `allow-transfer {"none";};`
    * `allow-recursion {"none";};`
    * `recursion no;`
1. Restart the device.
