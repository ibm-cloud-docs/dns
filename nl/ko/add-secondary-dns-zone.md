---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, IBM Cloud, Add Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 보조 DNS 구역 추가
{:#add-a-secondary-dns-zone}

{{site.data.keyword.BluSoftlayer_notm}}는 데이터 유실 시에 기본 DNS 구역을 캐싱하는 수단으로 보조 DNS를 모든 고객에게 제공합니다. 보조 DNS 구역 유지보수가 필수는 아니지만, 다중 도메인을 갖는 사용자의 경우에는 강력히 추천합니다. 보조 DNS 구역을 추가하려면 아래의 단계를 따르십시오.

* 탐색 메뉴에서 **클래식 인프라**를 선택하여 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **보조 DNS 구역** 화면으로 이동하십시오. 
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > 보조 구역**을 선택하십시오.
* **구역 추가** 탭을 선택하십시오.
* **구역** 필드에 **구역에 대한 도메인**을 입력하십시오.
* **마스터 이름 서버** 필드에 **마스터 이름 서버의 IP 주소**를 입력하십시오.
* **전송 간격** 필드에서 기본 DNS 구역이 보조 DNS 구역으로 전송할 **전송 시간**(분 단위)을 입력하십시오.
* **추가** 단추를 선택하여 구역을 추가하거나, **취소**를 선택하여 조치를 취소하십시오.

## 다음 작업
{:#add-a-secondary-dns-zone-next}

보조 DNS 구역은 작성된 후 보조 DNS 구역 화면의 구역 목록에 나타납니다. 기본 구역에서 보조 구역으로의 데이터 전송은 구역이 작성될 때 사용자가 지정한 간격으로 발생합니다. 언제든지 구역을 [편집](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record), [수동으로 전송](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) 또는 구역을 기본 구역으로 [변환](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone)할 수 있습니다. 보조 DNS 구역은 또한 언제든지 [삭제](/docs/infrastructure/dns?topic=dns-delete-a-secondary-dns-zone)할 수 있습니다.
