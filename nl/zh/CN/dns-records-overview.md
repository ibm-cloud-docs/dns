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

# DNS 概述 - 资源记录
{:#dns-0verview-resource-records}

## `A` 记录部分
{:#the-a-record-section}

大多数记录都是 **A** 记录。这样一来，您可以极度灵活地将域名指向所需的任意位置。每个记录都包含一个主机名和一个 IP 地址。

**主机字段：**该特定 A 记录的主机名。在 FQDN（标准域名）中，主机名应该是 _.domain.com_ 前面的内容。例如，在 `www.domain.com` 上，“www”是主机（不含引号）。不管此字段中列出的是什么内容，查找操作都会自动向查询附加“.domain.com”。通过在“主机名”字段中输入“@”号可创建空白的“A 记录”（_domain.com_，而不是 _host.domain.com_）。

常见“A”记录包括：`www.domain.com`、`ftp.domain.com`、`mail.domain.com`、`webmail.domain.com` 和 `mysql.domain.com`

**指向字段：**此字段用于列出主机名应该指向的 IP 地址。

## `CNAME` 部分
{:#the-cname-section}

CNAME 记录指向域名而不是 IP 地址。使用 CNAME 记录的好处是，可以将主机指向特定的域名，然后仅修改目标域名的 A 记录，从而使更改在这两个域上同时生效。此方法通常由在同一个域的不同版本（.com、.net、org）中拥有几个顶级域 (TLD) 的用户使用。

例如，您拥有 `_domain.com_`，同时还拥有 `_domain.net_`，并且您希望这些记录指向同一 IP。您可以为 `_domain.net_` 的 _www_ 主机创建指向 `www.domain.com` 的 CNAME 记录。然后，要更改 `_domain.net_` 的 _www_ 主机，您只需将 A 记录 `www.domain.com` 修改为指向其新 IP 地址，`www.domain.net` 就会自动进行更改。

使用此方法时，常犯的错误是您只打算更改一个域，但结果却意外地修改了多个域的记录。也就是说，您_必须_记下哪些域指向彼此。

**主机字段：**该特定 CNAME 记录的主机名。主机名应该是 FQDN 中 .domain.com 前面的内容。例如，在 `www.domain.com` 上，“www”是主机（不含引号）。不管此处列出的是什么内容，查找操作都会自动向查询附加“`.domain.com`”。通过在“主机名”字段中输入 `@` 号可创建空白的“A 记录”（`_domain.com_`，而不是 `_host.domain.com_`）。

**指向字段：**记录指向的名称。_此字段必须是域名，而不能是 IP 地址。_域名还必须以点结尾。否则，查询时，域记录将继续，直到发现区域文件的下一个点。

## `MX` 部分
{:#the-mx-section}

MX 部分是用于处理邮件方向的区域。

**优先级字段：**此部分允许您为单个 MX 记录选择优先权。记录会按顺序进行处理，首先处理最低优先级，然后处理较高的优先级。因此，如果您有两个邮件服务器或者有一个邮件服务器和一个邮件假脱机程序，请为主邮件服务器设置较低优先级，为备份邮件服务器或邮件假脱机程序设置较高优先级。

**主机字段：**可以在此处指定邮件主机名，但大多数情况下不必这样做。建议创建空白主机（使用 `@` 作为主机名），并将其指向邮件服务器。

**转至字段：**邮件服务器的地址。在此通常执行的操作是使用您在 A 记录部分中创建的邮件主机名来指向邮件。

强烈建议将 MX 记录指向域名，并且该域名（就像 CNAME 记录一样）必须以点结尾。

## `TXT` 部分
{:#the-txt-section}

TXT 记录通常是可以查询的记录，会返回有关域的信息。这些记录可用于指示 SPF，用于建立端口和协议连接，或者仅用于返回有关域的信息。TXT 记录最常与 SPF 协议一起使用。

**名称：**可以按其查询 TXT 记录的主机。

**值：**TXT 记录将返回的内容，内容会加有引号。
