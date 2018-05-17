---
copyright:
  years: 1994, 2017
lastupdated: "2018-05-17"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

<a name="top"></a>
# DNS FAQ

## What are the DNS servers?

161.26.0.10 and 161.26.0.11

## What are the local DNS Resolvers?

The local resolving nameservers on our private network are:

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

These nameservers provide fast domain name resolution that doesn't use up your public bandwidth allotment. To use them, please follow the correct procedure for adding resolving nameservers to your operating system.

## What are the {{site.data.keyword.BluSoftlayer_notm}} name server addresses?

We have two addresses for Authoritative Name Servers and two addresses for Resolving Name Servers.

### Authoritative Name Servers

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### Resolving Name Servers

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

These local resolving nameservers are on our private network, so they don't use up your public bandwidth allotment. 

## What IBM Cloud DNS servers will answer for my secondary domains?

The {{site.data.keyword.BluSoftlayer_notm}} Anycast, IPv-enabled Authoritative DNS Servers will answer for your secondary domains. These servers are found at the following addresses:

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## Which IP addresses will be used for my secondary domain zone transfers?

Transfers for your secondary domains will come from one of the following four IP addresses:

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## What is the difference between the public and private name servers?

Our public name servers act as authoritative name servers for domain names that reside in our DNS servers and are managed through the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). These servers "answer" and "resolve" domain names to your IP address for the general internet population.

Our resolving name servers are located on the private network and act as DNS resolvers for your server. The private resolvers query the Internet's root nameservers for domain lookups. For example, sending mail from your server requires an NSlookup of the destination domain name. The private DNS servers resolve this information over the private network to keep your bandwidth usage down, reduce the load on the authoritative servers, and offer quick resolution. Private network resolvers are a convenience service for our customers.

## What are my name server options?

With a Bare Metal Server there are four typical options for name servers:

* Use your domain name registrar's name servers to manage your domain names.
* Use {{site.data.keyword.BluSoftlayer_notm}} name servers to manage your domain names.
* Use a third-party DNS service to manage your domain names.
* Run your own name servers on your server to manage your domain names.

For the first three options, you will use name servers of the third party (for example, `ns1.softlayer.com` and `ns2.softlayer.com`). The last option uses your domain as the name server (for example, `ns1.yourdomain.com` & `ns2.yourdomain.com`), and it requires you to run DNS services on your server. You must also register your domain as a name server with your registrar. Nameserver registration is usually free, but it requires an additional step beyond the basic domain name registration process.

Our customers have free DNS services that are fully managed through the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/). We highly recommend allowing {{site.data.keyword.BluSoftlayer_notm}} to manage your DNS and your name servers, due to our redundant systems, ease of management, and ability to troubleshoot DNS-related issues quickly.

## How do I set up my Reverse DNS?

Reverse DNS setup takes place using our [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/)  For instructions on how to set up your Reverse DNS, refer to [Update a Reverse DNS Record](update-reverse-dns.html).

<a name="29"></a>
## How long does it take for DNS changes to propagate?

DNS change propagation times depend on the time-to-live (TTL) setting for the DNS record.

The default TTL is one day, which means any modifications to a domain name take one day to propagate throughout the entire internet. TTL can be lowered if you plan to make changes frequently, however, the lower the TTL is, the higher the load becomes on the name server. Higher loads have a potential to increase the response time to end users, which could impact their overall satisfaction.

The higher the TTL setting, the higher DNS performance will be due to local ISP caching. The lower the TTL setting, the lower DNS performance will be due to increased name resolution.

To verify TTL, check the Start of Authority (SOA) record for the domain. A great tool for reviewing domain information is offered by [CentralOps.net](http://centralops.net/co/)

TTL is listed in seconds.Divide by 60 to convert TTL to minutes, or by 3600 to convert to hours.

[Back to Top](#top)


## After transferring a domain, how long does it take for the domain and the changes made to become visible?

Your domain and/or changes to it are visible on IBM Cloud DNS servers immediately after the transfer completes. Due to the propagation nature of DNS, there will be a delay before changes are visible on other DNS servers.

## Can I complete AXFR requests on the private network?

Currently, {{site.data.keyword.BluSoftlayer_notm}} does not support AXFR request on the private network. All AXFR requests must be completed on the public network.
