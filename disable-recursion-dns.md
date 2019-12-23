---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Disable Recursion, DNS IBM Cloud DNS servers, BIND configuration file

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Disable Recursion for DNS
{:#disable-recursion-for-dns}

IBM Cloud DNS servers perform recursion by default. Recursion allows your DNS server to contact other DNS servers to assist in resolving domain names when it cannot resolve the domain itself. Recursion can prove to be useful tool when it is necessary; however, it also opens the DNS server open to attack, which could take down the DNS server altogether. System administrators  generally identify a need for recursion and act accordingly. Otherwise, it is best to disable recursion. Follow the steps below based on your operating system or control panel to disable DNS recursion.

## Disable Recursion in Plesk
{:#disable-recursion-in-plesk}
1. Log into the **Plesk Admin Panel**.
1. Select **Tools and Settings**.
1. Click **DNS Template Settings** from the section.
1. Select **Localnets** from the **DNS Recursion** section.
1. Click the **OK** button.

## Disable Recursion in Windows Server 2003 and 2008
{:#disable-recursion-in-windows-server}

1. Use the **DNS Manager** from the **Start** menu:
  * Click the **Start** button.
  * Select **Administrative Tools**.
  * Select **DNS**.
1. Right click on the desired **DNS Server** in the **Console Tree**.
1. Select the **Properties** tab.
1. Click the **Advanced** button in the **Server Options** section.
1. Select the **Disable Recursion** checkbox.
1. Click the **OK** button.

## Disable Recursion in Linux
{:#disable-recursion-in-linux}

1. Locate the BIND configuration file within the operating system. The BIND configuration file is usually located in one of the following paths:
  * /etc/bind/named.conf
  * /etc/named.conf

1. Open the named.conf file in your preferred editor.
1.  Add the following details to the **Options** section:
  * `allow-transfer {"none";};`
  * `allow-recursion {"none";};`
  * `recursion no;`
1. Restart the device.
