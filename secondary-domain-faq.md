---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-07"

keywords: Secondary Domain FAQ, zone transfers, IBM Cloud DNS servers

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Secondary Domain FAQ
{:#secondary-domain-faq}

## What IBM Cloud DNS servers will answer for my secondary domains?
{:#what-ibm-cloud-dns-servers-will-answer-for-my-secondary-domains}

IBM Cloud's Anycast, IPv6-enabled, Authoritative DNS Servers:

 * ns1.softlayer.com
 * ns2.softlayer.com

## Where will the zone transfers come from?
{:#where-will-the-zone-transfers-come-from}

Transfers of your secondary domain's will come from one of four IP addresses:

  * 66.228.118.67
  * 67.228.119.235
  * 208.43.119.235
  * 12.96.161.249

## How long, after transferring a domain, does it take for that domain or changes to it to become visible?
{:#how-long-does-it-take-for-changes-to-become-visible}

The domain and any changes to it will be visible on IBM Cloud DNS servers immediately after the transfer completes. Due to the caching and propagation nature of DNS, it may take a while for those changes to be visible on other DNS servers.  

## Are zone update notifies supported?
{:#are-zone-update-notifies-supported}

Notifies are not supported at this time.

## How immediate is the Transfer Now button?
{:#how-immediate-is-the-transfer-now-button}

After clicking the transfer now button, the domain will be transferred a the beginning of the next minute.

## Can a master be configured on the private network or will it have to go through the public?
{:#can-a-master-be-configured-on-private-network}

Not at this time. All AXFR requests are made over the public network.

## Are slaves removed after a number of days in which the master is unavailable?
{:#are-slaves-removed-after-days-master-is-unavailable}

We will stop attempting to transfer a domain if its master is down or misconfigured for a prolonged period.  The portal provides customer feedback (the Error Messages tab) and a method of reactivating  a domain (the Manual Zone Transfer tab) in the event there's issues transferring the zone and it is disabled as a consequence.

## Is 1 minute the lowest transfer frequency?
{:#is-1minute-lowest-transfer-frequency}

Yes.

## If frequency is set to 1920 minutes, then back to 10, will the 1920 minutes have to expire first before the new frequency goes into effect?
{:#frequency-change-expiration-effects}

No. The system calculates the retransfer queue by taking the time of our last transfer attempt and adding the frequency to it.  So, if you have frequency set to 1920 and you then change it to 10 minutes, as long as it's been at least 10 minutes since we last tried to transfer, we will retry immediately and then every 10 minutes thereafter.
