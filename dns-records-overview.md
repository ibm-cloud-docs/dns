---

copyright:
  years: 1994, 2020
lastupdated: "2020-04-23"

keywords: 

subcollection: dns

---

{{site.data.keyword.attribute-definition-list}}

# About resource records
{: #dns-overview-resource-records}

Resource records provide information about the components that support your domain, and are used to resolve all DNS queries.  
{: shortdesc}

## `A` records
{: #the-a-record-section}

Most records are **A** records. This allows the greatest versatility in pointing your domain names where you want them go. Each record consists of a hostname and an IP address.

**Host field:** The hostname for that particular **A** record. The hostname should be what precedes the _.domain.com_ in your FQDN (fully qualified domain name). For instance, on `www.domain.com`, `www` is the host. Whatever is listed here, the lookup automatically appends `.domain.com` to the query. A blank **A** record ( _domain.com_ rather than _host.domain.com_) is created by putting a `@` sign in the hostname field.

Common **A** records include: `www.domain.com`, `ftp.domain.com`, `mail.domain.com`, `webmail.domain.com`, `mysql.domain.com`

**Points to field:** This field is where you list the IP address to which the hostname should point.

## `CNAME` records
{: #the-cname-section}

`CNAME` records point to domain names instead of IP addresses. The benefit of using a `CNAME` record is that you can point a host to a particular domain name, then only modify the target domain name’s **A** records to have the change take place on both domains. This method is commonly used by those who own several top-level domains (TLD) in different versions (.com, .net, .org, etc.) of the same domain.

For example, you own `domain.com` and you also own `domain.net`, and you want the records to point to the same IP address. You can create `CNAME` records for the _www_ host of `domain.net` that point to `www.domain.com`. Then, to change the _www_ host of `domain.net` all you do is modify the **A** record of `www.domain.com` to point to its new IP address, and `www.domain.net` is automatically updated.

A common mistake when using this method is that you can accidentally modify the records for several domains when you intend to change only one. That is, you _must_ make a note of which domains point to each other. Also, a record cannot be created with same name as an existing CNAME record.

**Host field:** The hostname for that particular `CNAME` record. The hostname should be what precedes the _.domain.com_ in your FQDN. For instance, on `www.domain.com`, `www` is the host. Whatever is listed here, the lookup automatically appends `.domain.com` to the query. A blank **A** record (`domain.com` rather than `host.domain.com`) is created by putting a `@` sign in the hostname field.

**Points to field:** The name that the record points to. _This field must be a domain name, and not an IP address._ The domain name must also end with a dot. Otherwise, when queried, the domain record will continue until it finds the next dot in the zone file.

## `MX` records
{: #the-mx-section}

An `MX` record handles the direction of mail.

**Priority field:** This section allows you to select your preference for an individual `MX` record. Records are processed in order, starting with the lowest priority and working to higher priorities. Therefore, if you have two mail servers or a mail server and a mail spooler, set the lower priority to your main mail server and set a higher priority to your backup mail server or mail spooler.

**Host field:** You can specify a mail hostname here, but in most cases, it is not necessary. It is recommended to create a blank host (use a `@` for the hostname) and point it to your mail server.

**Goes to field:** The address of the mail server. What is commonly done here is using the mail hostname that you created in the **A** record section to point to your mail server.

It is highly recommended that you point `MX` records to a domain name, and that domain name (just like a `CNAME` record) ends with a dot.

## `TXT` records
{: #the-txt-section}

A `TXT` record generally is a record that you can query, and which returns information about a domain. These records can be used for SPF indicators, for crafting port and protocol connections, or just for returning information about a domain. They are most commonly used with the SPF protocol.

**Name:** The host that the `TXT` record can be queried by.

**Value:** What the TXT record returns, placed in quotes.
