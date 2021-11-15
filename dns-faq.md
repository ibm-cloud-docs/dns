---

copyright:
  years: 1994, 2021
lastupdated: "2021-02-05"

keywords:

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# DNS FAQs
{: #dns-faq}

Frequently asked questions for DNS and Domain Name Registration might include questions about server addresses, name server options, and other common inquiries. To find all FAQs for {{site.data.keyword.cloud}}, see our [FAQ library](/docs/faqs).
{: shortdesc}

## What are the DNS servers?
{: #what-are-dns-servers}
{: faq}
{: support}

The DNS servers are `161.26.0.10` and `161.26.0.11`.

## What are the local (or private) IBM Cloud DNS resolvers?
{: #what-are-local-dns-resolvers}
{: faq}
{: support}

The local resolving name servers on the {{site.data.keyword.cloud_notm}} private network are:

* `rs1.service.softlayer.com 10.0.80.11`
* `rs2.service.softlayer.com 10.0.80.12`

These local resolving name servers are on our private network, so they don't use up public bandwidth.

## What are the IBM Cloud name server addresses?
{: #what-are-name-server-addresses}
{: faq}
{: support}

IBM has two addresses for authoritative name servers and two addresses for resolving name servers. These local resolving name servers are on the IBM private network, so they don't use up public bandwidth.

* **Authoritative name servers**
    * `ns1.softlayer.com 67.228.254.4`
    * `ns2.softlayer.com 67.228.255.5`

* **Resolving name servers**
    * `rs1.service.softlayer.com 10.0.80.11`
    * `rs2.service.softlayer.com 10.0.80.12`

## What IBM Cloud DNS servers will answer for my secondary domains?
{: #what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}
{: support}

The IBM Cloud Anycast, IPv-enabled authoritative DNS Servers will answer for your secondary domains. These servers are found at the following addresses:

* `ns1.softlayer.com`
* `ns2.softlayer.com`

## Which IP addresses are used for my secondary domain zone transfers?
{: #which-ipaddresses-secondary-domain-zone-transfers}
{: faq}
{: support}

Transfers for your secondary domains come from one of the following four IP addresses:

* `66.228.118.67`
* `67.228.119.235`
* `208.43.119.235`
* `12.96.161.249`

## What is the difference between the public and private name servers?
{: #public-v-private-nameservers}
{: faq}
{: support}

Our public name servers act as authoritative name servers for domain names that reside in our DNS servers and are managed through the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/). These servers answer and resolve domain names to your IP address for the general internet population.

Our resolving name servers are located on the private network and act as DNS resolvers for your server. The private resolvers query the internet's root name servers for domain lookups. For example, sending mail from your server requires an NSlookup of the destination domain name. The private DNS servers resolve this information over the private network to keep your bandwidth usage down, reduce the load on the authoritative servers, and offer quick resolution. Private network resolvers are a convenience service for our customers.

## What are my name server options?
{: #what-are-my-name-server-options-faq}
{: faq}
{: support}

With a bare metal server there are four typical options for name servers:

* Use your domain name registrar's name servers to manage your domain names.
* Use {{site.data.keyword.cloud_notm}} name servers to manage your domain names.
* Use a third-party DNS service to manage your domain names.
* Run your own name servers on your server to manage your domain names.

For the first three options, you will use name servers of the third party (for example, `ns1.softlayer.com` and `ns2.softlayer.com`). The last option uses your domain as the name server (for example, `ns1.yourdomain.com` and `ns2.yourdomain.com`), and it requires you to run DNS services on your server. You must also register your domain as a name server with your registrar. Name server registration is usually free, but it requires an additional step beyond the basic domain name registration process.

Our customers have free DNS services that are fully managed through the [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/). It is highly recommended that you allow {{site.data.keyword.cloud_notm}} to manage your DNS and your name servers, due to our redundant systems, ease of management, and ability to troubleshoot DNS-related issues quickly.

## How do I renew my domain name?
{: #renew-domain}
{: faq}
{: support}

To renew a registration for an existing domain, select [**Classic Infrastructure**](https://{DomainName}/gen1/infrastructure/devices) from the menu in the {{site.data.keyword.cloud_notm}} console, and then go to **Services > Domain Registration**. See [Renewing existing domains](/docs/dns?topic=dns-renew-an-existing-domain).

## How do I manage DNS zones?
{: #manage-domain}
{: faq}
{: support}

Using the DNS interface, you can manage Forward Zones, Secondary Zones, and Reverse Records. To use this interface, select [**Classic Infrastructure**](https://{DomainName}/gen1/infrastructure/devices) from the menu in the {{site.data.keyword.cloud_notm}} console, and then go to **Network > DNS**.


## How do I set up my reverse DNS?
{: #how-do-i-setup-reverse-dns}
{: faq}

Reverse DNS setup takes place using our [{{site.data.keyword.cloud_notm}} console](https://{DomainName}/). For instructions on how to set up your reverse DNS, refer to [Managing reverse DNS records](/docs/dns?topic=dns-add-or-edit-a-ptr-pointer-record).


## How long does it take for DNS changes to propagate?
{: #how-long-for-dns-changes-propagate}
{: faq}

DNS change propagation times depend on the time-to-live (TTL) setting for the DNS record. The default TTL is one day, which means any modifications to a domain name take one day to propagate throughout the entire internet. TTL can be lowered if you plan to make changes frequently; however, the lower the TTL is, the higher the load becomes on the name server. Higher loads have a potential to increase the response time to end users, which could impact their overall satisfaction.

The higher the TTL setting, the higher DNS performance is due to local ISP caching. The lower the TTL setting, the lower DNS performance is due to increased name resolution.

To verify TTL, check the Start of Authority (SOA) record for the domain. A great tool for reviewing domain information is offered by [CentralOps.net](http://centralops.net/co/){: external}

TTL is listed in seconds. Divide by 60 to convert TTL to minutes, or by 3600 to convert to hours.


## After transferring a domain, how long does it take for the domain and the changes made to become visible?
{: #how-long-transfer-change-visiblity}
{: faq}

Your domain and/or changes to it are visible on IBM Cloud DNS servers immediately after the transfer completes. Due to the propagation nature of DNS, there will be a delay before changes are visible on other DNS servers.

## Can I complete AXFR requests on the private network?
{: #axfr-request-private-network}
{: faq}

Currently, {{site.data.keyword.cloud_notm}} does not support AXFR request on the private network. All AXFR requests must be completed on the public network.

## How can I run my own name servers?
{: #how-can-i-run-my-own-nameservers}
{: faq}

The easiest way to run and manage your own name servers is to use a control panel tool such as **Plesk** or **cPanel**. Both of these products have built in domain name servers that allow you to add, modify, or delete domain names.

To begin, register your domain name as a name server with your domain name registrar and assign two IP addresses from your server IP ranges.

## Are zone update notifies supported for secondary DNS zones?
{: #are-zone-update-notifies-supported}
{: faq}

Zone update notifies are not supported at this time.

## How immediate is the transfer now button for secondary DNS zones?
{: #how-immediate-is-the-transfer-now-button}
{: faq}

After clicking the transfer now button, the domain will be transferred at the beginning of the next minute.

## Can a master be configured on the private network or does it have to go through the public?
{: #can-a-master-be-configured-on-private-network}
{: faq}

All AXFR requests are made over the public network at this time.

## Are slaves removed after a number of days in which the master is unavailable?
{: #are-slaves-removed-after-days-master-is-unavailable}
{: faq}

IBM stops attempting to transfer a domain if its master is down or misconfigured for a prolonged period. You can view errors in the IBM Cloud console and force a manual transfer.

## Is 1 minute the lowest transfer frequency for secondary DNS zones?
{: #is-1minute-lowest-transfer-frequency}
{: faq}

The lowest transfer frequency is 1 minute.

## If frequency is set to 1920 minutes, then back to 10, will the 1920 minutes expire before the new frequency goes into effect?
{: #frequency-change-expiration-effects}
{: faq}

The system calculates the retransfer queue by taking the time of our last transfer attempt and adding the frequency to it.  So, if you have frequency set to 1920 and you then change it to 10 minutes, as long as it's been at least 10 minutes since the system last tried to transfer, it retries immediately and then every 10 minutes thereafter.
