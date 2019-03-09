---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: domain names, Resource Records, host name

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS Overview - Resource Records
{:#dns-0verview-resource-records}

## The `A` record section
{:#the-a-record-section}

Most records will be **A** records. This allows the greatest versatility in pointing your domain names where you want them go. Each record consists of a host name and an IP address.

**Host field:** The host name for that particular A record. The host name should be what precedes the _.domain.com_ in your FQDN (fully qualified domain name). For instance, on `www.domain.com`, "www" is the host (without the quotation marks). Whatever is listed here, the lookup will automatically append “.domain.com” to the query. A blank "A record" ( _domain.com_ rather than _host.domain.com_) is created by putting a '@' sign in the host name field.

Common "A" records include: `www.domain.com`, `ftp.domain.com`, `mail.domain.com`, `webmail.domain.com`, `mysql.domain.com`

**Points to field:** This field is where you list the IP address to which the host name should point.

## The `CNAME` section
{:#the-cname-section}

CNAME records point to domain names instead of IP addresses. The benefit to using a CNAME record is that you can point a host to a particular domain name, then only modify the target domain name’s A records to have the change take place on both domains. This method commonly is used by those who own several top-level domains (TLD) in different versions (.com, .net, .org, etc.) of the same domain.

For example, you own `_domain.com_` and you also own `_domain.net_`, and you want the records to point to the same IP. You can create CNAME records for the _www_ host of `_domain.net_` that point to `www.domain.com`. Then, to change the _www_ host of `_domain.net_` all you must do it modify the A record of `www.domain.com` to point to its new IP address, and `www.domain.net` also is automatically changed.

A common mistake to using this method is that you can accidentally modify the records for several domains when you only intend to change one. That is, you _must_ make a note of which domains point to each other.

**Host field:** The host name for that particular CNAME record. The host name should be what precedes the .domain.com in your FQDN. For instance, on `www.domain.com`, “www” is the host (without the quotation marks). Whatever is listed here, the lookup will automatically append “`.domain.com`” to the query. A blank "A record" (`_domain.com_` rather than `_host.domain.com_`) is created by putting a `@` sign in the host name field.

**Points to field:** The name that the record points to. _This field must be a domain name, and not an IP address._ The domain name must also end with a dot. Otherwise, when queried, the domain record will continue until it finds the next dot in the zone file.

## The `MX` section
{:#the-mx-section}

The MX section is the area that handles the direction of mail.

**Priority field:** This section allows you to select your preference for an individual MX record. Records are processed in order, starting with the lowest priority and working to higher priorities. Therefore, if you have two mailservers or a mailserver and a mail spooler, set the lower priority to your main mailserver and set a higher priorty to your backup mailserver or mail spooler.

**Host field:** You can specify a mail host name here, but in most cases it is not necessary. What is recommended is to create a blank host (use a `@` for the host name) and point it to your mail server.

**Goes to field:** The address of the mail server. What is commonly done here is using the mail hostname you created in the A record section to point your mail.

It is highly recommended that you point MX records to a domain name, and that domain name (just like a CNAME record) must end with a dot.

## The `TXT` section
{:#the-txt-section}

A TXT record generally is a record that you can query, and which returns information about a domain. These records can be used for SPF indicators, for crafting port and protocol connections, or just for returning information about a domain. They are most commonly used with the SPF protocol.

**Name:** The host that the TXT record can be queried by.

**Value:** What the TXT record will return, placed in quotes.
