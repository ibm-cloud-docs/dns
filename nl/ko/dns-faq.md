---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-04-10"

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


# DNS FAQ
{:#dns-faq}

## DNS 서버는 무엇입니까?
{:#what-are-dns-servers}
{: faq}

161.26.0.10 및 161.26.0.11

## 로컬 DNS 해석기는 무엇입니까?
{:#what-are-local-dns-resolvers}
{: faq}

자사의 사설 네트워크의 로컬 해석 이름 서버는 다음과 같습니다.

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

이들 이름 서버는 공용 대역폭 할당을 사용하지 않는 빠른 도메인 이름 해석을 제공합니다. 이들을 사용하려면 운영 체제에 해석 이름 서버 추가를 위한 올바른 프로시저를 따르십시오.

## {{site.data.keyword.BluSoftlayer_notm}} 이름 서버 주소는 무엇입니까?
{:#what-are-name-server-addresses}
{: faq}

인증된 이름 서버를 위한 두 개의 주소와 해석 이름 서버를 위한 두 개의 주소를 갖고 있습니다.

### 인증된 이름 서버
{:#authoratative-name-servers}

* ns1.softlayer.com 67.228.254.4
* ns2.softlayer.com 67.228.255.5

### 해석 이름 서버
{:#resolving-name-servers}

* rs1.service.softlayer.com 10.0.80.11
* rs2.service.softlayer.com 10.0.80.12

이들 로컬 해석 이름 서버는 자사의 사설 네트워크에 있으므로, 사용자의 공용 대역폭 할당을 사용하지 않습니다. 

## 어떤 IBM Cloud DNS 서버가 내 보조 도메인에 대해 응답합니까?
{:#what-ibm-cloud-dns-server-answers-for-secondary-domain}
{: faq}

{{site.data.keyword.BluSoftlayer_notm}} Anycast, IPv 가능 인증된 DNS 서버가 사용자 보조 도메인에 대해 응답합니다. 이들 서버는 다음 주소에서 발견됩니다.

  * ns1.softlayer.com
  * ns2.softlayer.com
  
## 내 보조 도메인 구역 전송을 위해 어떤 IP 주소가 사용됩니까?
{:#which-ipaddresses-secondary-domain-zone-transfers}
{: faq}

보조 도메인에 대한 전송은 다음 4개의 IP 주소 중 하나로부터 옵니다.

* 66.228.118.67
* 67.228.119.235
* 208.43.119.235
* 12.96.161.249

## 공용 이름 서버와 사설 이름 서버 사이의 차이점은 무엇입니까?
{:#public-v-private-nameservers}
{: faq}

공용 이름 서버는 자사의 DNS 서버에 상주하며 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)을 통해 관리되는 도메인 이름에 대한 인증된 이름 서버로 작용합니다. 이들 서버는 일반 인터넷 사용 인구에 대해 도메인 이름에 "응답"하고 이를 사용자의 IP 주소로 "해석"합니다.

해석 이름 서버는 사설 네트워크에 위치하며 사용자 서버를 위한 DNS 해석기로 작용합니다. 사설 해석기는 도메인 검색을 위해 인터넷의 루트 이름 서버를 조회합니다. 예를 들어, 서버에서 메일을 발송하려면 대상 도메인 이름의 NSlookup이 필요합니다. 사설 DNS 서버가 사설 네트워크를 통해 이 정보를 해석하여 사용자의 대역폭 사용량을 줄이고 인증 서버의 로드를 축소하며 빠른 해석을 제공합니다. 사설 네트워크 해석기는 고객을 위한 편의 서비스입니다.

## 내 이름 서버 옵션은 무엇입니까?
{:#what-are-my-name-server-options-faq}
{: faq}

Bare Metal Server를 사용할 때 이름 서버에 대한 다음 4가지 옵션이 있습니다.

* 도메인 이름 등록자의 이름 서버를 사용하여 도메인 이름을 관리합니다.
* {{site.data.keyword.BluSoftlayer_notm}} 이름 서버를 사용하여 도메인 이름을 관리합니다.
* 서드파티 DNS 서비스를 사용하여 도메인 이름을 관리합니다.
* 사용자 서버에서 사용자 고유의 이름 서버를 실행하여 도메인 이름을 관리합니다.

처음 세 옵션의 경우, 서드파티의 이름 서버(예: `ns1.softlayer.com` 및 `ns2.softlayer.com`)를 사용합니다. 마지막 옵션은 사용자의 도메인을 이름 서버로 사용하며(예: `ns1.yourdomain.com` & `ns2.yourdomain.com`), 사용자가 자신의 서버에서 DNS 서비스를 실행해야 합니다. 또한 자신의 도메인을 등록자에게 이름 서버로 등록해야 합니다. 이름 서버 등록은 대개 무료이지만, 기본 도메인 이름 등록 프로세스 이상의 추가 단계가 필요합니다.

자사의 고객은 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)을 통해 완전히 관리되는 무료 DNS 서비스를 갖습니다. 자사의 중복 시스템, 관리 용이성 및 DNS 관련 문제를 빨리 해결하는 능력으로 인해 {{site.data.keyword.BluSoftlayer_notm}}가 사용자의 DNS 및 이름 서버를 관리하도록 허용할 것을 강력히 권장합니다.

## 역방향 DNS를 어떻게 설정합니까?
{:#how-do-i-setup-reverse-dns}
{: faq}

역방향 DNS 설정은 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)에서 발생합니다. 역방향 DNS를 설정하는 방법에 대한 지시사항은 [역방향 DNS 레코드 업데이트](/docs/infrastructure/dns?topic=dns-update-reverse-dns-record)를 참조하십시오.


## DNS 변경이 전파하는 데 얼마나 걸립니까?
{:#how-long-for-dns-changes-propagate}
{: faq}

DNS 변경 전파 시간은 DNS 레코드에 대한 TTL(Time to Live) 설정에 따라 다릅니다.

기본 TTL은 1일입니다. 이것은 도메인 이름에 대한 모든 수정사항이 전체 인터넷을 통해 전파하는 데 하루가 걸림을 의미합니다. 변경사항을 자주 작성할 계획인 경우 TTL을 낮출 수 있지만, TTL이 낮을수록 이름 서버에 대한 로드가 더 높아집니다. 더 높은 로드는 일반 사용자에게 응답 시간을 증가시킬 위험성을 갖고 있어서 전체 만족도에 영향을 미칠 수 있습니다.

TTL 설정이 높을수록, 로컬 ISP 캐싱 때문에 DNS 성능이 더 높아집니다. TTL 설정이 낮을수록, 증가된 이름 해석 때문에 DNS 성능이 더 낮습니다.

TTL을 확인하려면 도메인의 권한 개시 정보(SOA) 레코드를 확인하십시오. 도메인 정보 검토를 위한 강력한 도구는 [CentralOps.net ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://centralops.net/co/)에서 제공합니다.

TTL은 초 단위로 나열됩니다. TTL을 분 단위로 변환하려면 60으로 나누거나, 시간 단위로 변환하려면 3600으로 나누십시오.


## 도메인을 전송한 후, 도메인 및 변경사항을 볼 수 있을 때까지 얼마나 걸립니까?
{:#how-long-transfer-change-visiblity}
{: faq}

도메인 및/또는 그에 대한 변경사항은 전송이 완료된 후 IBM Cloud DNS 서버에서 즉시 볼 수 있습니다. DNS의 전파 네이처로 인해 변경사항이 다른 DNS 서버에서 보이기 전에 지연이 있습니다.

## 사설 네트워크에서 AXFR 요청을 완료할 수 있습니까?
{:#axfr-request-private-network}
{: faq}

현재로서는, {{site.data.keyword.BluSoftlayer_notm}}는 사설 네트워크에서 AXFR 요청을 지원하지 않습니다. 모든 AXFR 요청은 공용 네트워크에서 완료되어야 합니다.
