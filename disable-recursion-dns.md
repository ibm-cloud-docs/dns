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
* Log into the **Plesk Admin Panel**.
* Select **Tools and Settings**.
* Click **DNS Template Settings** from the section.
* Select **Localnets** from the **DNS Recursion** section.
* Click the **OK** button.

## Disable Recursion in Windows Server 2003 and 2008
{:#disable-recursion-in-windows-server}

* Use the **DNS Manager** from the **Start** menu:
  * Click the **Start** button.
  * Select **Administrative Tools**.
  * Select **DNS**.
* Right click on the desired **DNS Server** in the **Console Tree**.
* Select the **Properties** tab.
* Click the **Advanced** button in the **Server Options** section.
* Select the **Disable Recursion** checkbox.
* Click the **OK** button.

## Disable Recursion in Linux
{:#disable-recursion-in-linux}

 * Locate the BIND configuration file within the operating system. The BIND configuration file is usually located in one of the following paths:
  * /etc/bind/named.conf
  * /etc/named.conf
* Open the named.conf file in your preferred editor.
* Add the following details to the **Options** section:<br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* Restart the device.
