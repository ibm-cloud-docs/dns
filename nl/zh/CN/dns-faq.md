---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-13"

keywords: DNS servers, fast domain name resolution, DNS FAQ

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}
{:faq: data-hd-content-type='faq'}


# DNS 常见问题
{:#dns-faq}

## 有哪些 DNS 服务器？
{:#what-are-dns-servers}
{: faq}

161.26.0.10 和 161.26.0.11

## 有哪些本地 DNS 解析器？
{:#what-are-local-dns-resolvers}
{: faq}

我们专用网络上的本地解析名称服务器为：

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

这些名称服务器能快速解析域名，而不会用尽您的公用带宽分配量。要使用这些名称服务器，请遵循用于将解析名称服务器添加到操作系统的正确过程。

## {{site.data.keyword.BluSoftlayer_notm}} 名称服务器的地址是什么？
{:#what-are-name-server-addresses}
{: faq}

有两个地址用于权威名称服务器，两个地址用于解析名称服务器。

### 权威名称服务器
{:#authoratative-name-servers}

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### 解析名称服务器
{:#resolving-name-servers}

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

这些本地解析名称服务器位于专用网络上，因此不会用尽您的公用带宽分配量。 

## 哪些 IBM Cloud DNS 服务器将应答辅助域？
{:#what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}

{{site.data.keyword.BluSoftlayer_notm}} 支持 IPv 的 Anycast 权威 DNS 服务器将应答辅助域。可以在以下地址找到这些服务器：

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## 哪些 IP 地址将用于辅助域区域传输？
{:#which-ipaddresses-secondary-domain-zone-transfers}
{: faq}

辅助域的传输将来自以下四个 IP 地址中的一个地址：

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## 公用和专用名称服务器有何区别？
{:#public-v-private-nameservers}
{: faq}

公用名称服务器充当位于 DNS 服务器中且通过[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 管理的域名的权威名称服务器。这些服务器“应答”域名并将其“解析”为 IP 地址以用于一般因特网填充内容。

解析名称服务器位于专用网络上，并充当服务器的 DNS 解析器。专用解析器查询因特网的根名称服务器以查找域。例如，从服务器发送邮件需要对目标域名执行 NSlookup。专用 DNS 服务器通过专用网络解析此信息，以使带宽使用量保持在低水平，减少权威服务器上的负载，并提供快速解析。专用网络解析器是我们为客户提供的一项便捷服务。

## 有哪些名称服务器选项？
{:#what-are-my-name-server-options-faq}
{: faq}

对于裸机服务器，名称服务器有四个典型选项：

* 使用域名注册器的名称服务器来管理域名。
* 使用 {{site.data.keyword.BluSoftlayer_notm}} 名称服务器来管理域名。
* 使用第三方 DNS 服务来管理域名。
* 在服务器上运行自己的名称服务器来管理域名。

对于前三个选项，都将使用第三方的名称服务器（例如，`ns1.softlayer.com` 和 `ns2.softlayer.com`）。最后一个选项将您的域用作名称服务器（例如，`ns1.yourdomain.com` 和 `ns2.yourdomain.com`），并且需要您在服务器上运行 DNS 服务。您还必须使用注册器将您的域注册为名称服务器。名称服务器注册通常是免费的，但除了基本域名注册过程外，还需要执行一个额外的步骤。

我们的客户拥有免费 DNS 服务，这些服务通过[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 进行完全管理。我们强烈建议允许 {{site.data.keyword.BluSoftlayer_notm}} 来管理 DNS 和您的名称服务器，因为我们有冗余系统，易于管理，并且能够快速对 DNS 相关问题进行故障诊断。

## 如何设置逆向 DNS？
{:#how-do-i-setup-reverse-dns}
{: faq}

使用[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/) 可执行逆向 DNS 设置。有关如何设置逆向 DNS 的指示信息，请参阅[更新逆向 DNS 记录](/docs/infrastructure/dns?topic=dns-update-reverse-dns-record)。


## 传播 DNS 更改需要多长时间？
{:#how-long-for-dns-changes-propagate}
{: faq}

DNS 更改的传播时间取决于 DNS 记录的生存时间 (TTL) 设置。

缺省 TTL 为 1 天，这意味着对域名进行的任何修改都需要一天的时间在整个因特网中进行传播。如果您计划频繁进行更改，那么可以降低 TTL，但是，TTL 越低，名称服务器上的负载越高。负载越高，对最终用户的响应时间有可能越长，这会影响最终用户的总体满意度。

TTL 设置越高，DNS 性能将由于本地 ISP 高速缓存而越高。TTL 设置越低，DNS 性能将由于名称解析增加而越低。

要验证 TTL，请检查域的“起始授权”(SOA) 记录。[CentralOps.net ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://centralops.net/co/) 提供了一个很不错的工具来查看域信息

这会列出 TTL（以秒为单位）。将值除以 60，可将 TTL 转换为以分钟为单位，或者除以 3600 以转换为以小时为单位。


## 传输域后，需要多长时间才会显示该域和所做的更改？
{:#how-long-transfer-change-visiblity}
{: faq}

传输完成后，IBM Cloud DNS 服务器上会立即显示该域和/或对其所做的更改。由于 DNS 的传播特性，在其他 DNS 服务器上显示更改之前，会有一定延迟。

## 可以在专用网络上完成 AXFR 请求吗？
{:#axfr-request-private-network}
{: faq}

目前，{{site.data.keyword.BluSoftlayer_notm}} 不支持在专用网络上完成 AXFR 请求。所有 AXFR 请求都必须在公用网络上完成。
