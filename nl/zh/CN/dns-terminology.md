---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Terminology, Caching, individual DNS servers, DNS resolver

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS 术语
{:#dns-terminology}

## 高速缓存和生存时间
{:#caching-and-time-to-live}

由于系统（如 DNS）会生成大量请求，因此设计人员提供了一种机制来减少单个 DNS 服务器上的负载，如下所示：

DNS 解析器（即客户机）收到 DNS 响应后，会将该响应高速缓存给定的时间段，此时间段称为生存时间（即 TTL）。TTL 的值由发出响应的 DNS 服务器的管理员进行设置。一旦响应进入高速缓存，解析器就会查询其高速缓存（存储）的应答；仅当 TTL 到期时（或者当管理员手动清空解析器内存中的响应时），解析器才会与 DNS 服务器联系以获取相同信息。

## 起始授权 (SOA) 记录参数
{:#soa-record-parameters}

通常，生存时间在“起始授权”(SOA) 记录中指定。SOA 参数包括：

### 序号
{:#soa-record-parameters-serial}

此区域文件的修订版号。每次更改区域文件后都会递增此编号，以便将更改分发到任何辅助 DNS 服务器。

### 刷新
{:#soa-record-parameters-refresh}

辅助名称服务器要检查域的主名称服务器中 DNS 区域新副本时应等待的时间长度（以秒为单位）。如果区域文件已更改，那么辅助 DNS 服务器将更新其区域副本，以与主 DNS 服务器的区域匹配。

### 重试
{:#soa-record-parameters-retry}

如果辅助名称服务器尝试刷新失败，在重试使用该辅助名称服务器刷新域的区域之前，域的一个或多个主名称服务器应该等待的时间长度（以秒为单位）。

### 到期
{:#soa-record-parameters-expire}

一个或多个辅助名称服务器可保留某个区域的时间长度（以秒为单位），在此之后将认为服务器对此区域没有权威。

### 最小值
{:#soa-record-parameters-minimum}

域的资源记录有效的时间长度（以秒为单位）。这也称为最小 TTL，可以由单个资源记录的 TTL 覆盖。

### TTL（生存时间）
{:#soa-record-parameters-ttl}

域名在本地高速缓存多长时间后到期（以秒为单位）；到期后，域名将返回到权威名称服务器以获取更新的信息。
