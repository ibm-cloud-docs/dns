---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Delete Secondary DNS Zones

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 보조 DNS 구역 삭제
{:#delete-a-secondary-dns-zone}

보조 DNS 구역이 작성된 후에는 언제든지 삭제할 수 있습니다. 보조 DNS 구역이 삭제되는 경우 검색할 수 없음을 유의하십시오. 보조 DNS 레코드를 삭제하려면 아래의 단계를 따르십시오.

 * 탐색 메뉴에서 **클래식 인프라**를 선택하여 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **보조 DNS 구역** 화면으로 이동하십시오. 
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > 보조 구역**을 선택하십시오.
* 삭제가 필요한 구역의 **조치** 드롭 다운 목록에서 **삭제**를 선택하십시오. 팝업 확인 상자가 나타납니다.
  다중 보조 구역이 있는 경우 보기를 필터링하여 삭제할 구역을 찾을 수 있습니다.
  {:note}
* **예** 단추를 선택하여 삭제를 확정하거나, **아니오**를 선택하여 조치를 취소하십시오.

## 다음 작업
{:#delete-a-secondary-dns-zone-next}

보조 DNS 구역이 삭제된 후에 기본 구역에서의 자동화된 전송은 중단되고 보조 구역은 더 이상 존재하지 않습니다. 언제든지 기본 구역에 대해 보조 DNS 구역이 필요한 경우 새 [보조 DNS 구역을 작성할 수 있습니다](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone).
