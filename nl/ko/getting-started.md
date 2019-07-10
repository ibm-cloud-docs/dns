---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-03"

keywords: IBM Cloud DNS, DNS

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS 시작하기 
{: #getting-started}

인터넷의 DNS(Domain Name System)는 서버 및 라우터가 인식하는 IP 주소를 사용자에게 친숙한 _도메인 이름_이라는 주어진 이름(예: `ibm.com`)으로 변환하는 방법입니다.

DNS의 개념은 단순하지만, 다양한 도메인에 대한 레코드를 관리 및 저장하는 편리한 방법이 없으면 이 작업은 매우 지루해질 수 있습니다.

IBM Cloud DNS는 고객에게 자사의 기본 DNS 관리 인터페이스를 사용하여 자신의 도메인을 보고 관리할 수 있는 중앙 위치를 제공합니다. 또한 사용자에게 동일한 위치에서 역방향 및 보조 DNS를 관리하는 옵션을 무료로 제공합니다.

IBM Cloud는 또한 추가 [네트워크 도구](/docs/infrastructure/network-tools?topic=network-tools-gettingstarted-with-network-tools#gettingstarted-with-network-tools) 모음을 제공합니다. [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)을 통해 DNS 인터페이스를 사용하는 데 관한 구체적인 지시사항은 [DNS 인터페이스 사용 방법](/docs/infrastructure/dns?topic=dns-how-to-use-the-dns-interface)을 참조하십시오.

## 작동 방식
{: #how-dns-works}

기본 레벨에서 {{site.data.keyword.BluSoftlayer_notm}} DNS는 사용자가 사용할 모든 DNS 관리 도구와 비슷하게 기능합니다. 기존 DNS 레코드와 상호작용하고 편집하며 새 레코드를 추가하고 역방향 DNS에 관한 정보를 업데이트하는 기능을 갖습니다. 다른 DNS 관리 서비스 또는 사용자 스스로 관리하는 것에 비해서도 {{site.data.keyword.BluSoftlayer_notm}} 사용의 주된 이점은 사용자의 모든 데이터가 저장되는 중앙 집중되고 신뢰할 수 있는 위치를 갖는다는 점입니다.

추가 서비스로서 {{site.data.keyword.BluSoftlayer_notm}}는 고객에게 보조 DNS 구역을 무료로 제공하므로, 사용자가 데이터 유실 또는 노드 장애 시에 기본 DNS 레코드를 백업할 수 있습니다.

## DNS 관리 방법
{: #how-to-manage-dns}

대부분의 사용자는 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)을 사용하여 기본, 역방향 및 보조 DNS를 관리합니다. 포털은 DNS의 모든 것을 관리하기 위해 마우스로 이용 가능한 인터페이스입니다.

또한 DNS 상호작용을 위해 IBM Cloud SoftLayer API(SLAPI)를 사용하는 옵션도 있습니다. 포털 UI와 비교할 때 이 API의 기능은 거의 동일합니다. 그러나 DNS 레코드를 대량으로 편집 중인 경우, 고객 포털은 최대 20개의 세트로 벌크화를 제공하지만, API는 더 많은 유연성을 제공합니다. SLAPI를 사용한 DNS 상호작용에 대한 자세한 정보는 [이 API 문서](/docs/infrastructure/dns?topic=dns-getting-started-with-the-dns-api#getting-started-with-the-dns-api)를 참조하십시오.


