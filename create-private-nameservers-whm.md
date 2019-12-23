---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Select Basic cPanel, Private Nameservers, name servers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Create private name servers in cPanel/WHM
{:#create-private-nameservers-in-cpanel-whm}

Using the cPanel/WHM product, you can create private name servers at any time. Private name servers allow the name servers associated with a website (for example, `www.yourdomain.com`) to display the website's name server (for example, `ns1.yourdomain.com`) instead of the name server associated with the web host for the website (for example `ns1.webhostdomain.com`). Adding a private name server to a domain also opens up additional options for DNS management within cPanel/WHM. Follow the steps in this article to create a private name server. If issues arise during or after the execution of this procedure, [open a case](/docs/get-support?topic=get-support-getting-customer-support).

## Name the name server
{:#name-the-nameserver}

* Log in to WHM on your server at the following URL: `http://xx.xx.xx.xx:2086`.
* Select **Basic cPanel/WHM Setup** from the **Server Configuration** menu.
* Enter the desired name server hostname(s) in one or more of the following fields:
  * Primary name server
  * Secondary name server
  * Tertiary name server
  * Quaternary name server
* Select the **Save** button.

## Create a Zone File for the Domain
{:#create-a-zone-file-for-the-domain}

* Select **Add a DNS Zone** from the **DNS Functions** menu.
* Enter the **IP address** for the domain in the **IP** field.
* Enter the **domain name** in the **Domain** field.

Alternately, a Domain Account may be created with the [Create an Account](https://docs.cpanel.net/display/70Docs/Create+a+New+Account) guide in cPanel's WHM documentation.
{:note}

## Assign an IP to the name server
{:#assign-an-ip-to-the-nameserver}

* Select **Name server IPs** from the **Network Setup** menu.
* Enter the first **name server name** in the **Name server** field.
* Select the **Assign** button.
* Repeat the steps above for each name server.

## Set up the name server
{:#setup-the-nameserver}

* Select **Name server setup** from the **Service Configuration** menu.
* Select the **Proceed** button on the pop-up message.
