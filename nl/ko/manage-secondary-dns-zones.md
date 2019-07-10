---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# 보조 DNS 구역 관리
{: #manage-secondary-dns-zones}

{{site.data.keyword.cloud}}는 데이터 유실 시에 기본 DNS 구역을 캐싱하는 수단으로 보조 DNS를 모든 고객에게 제공합니다. 보조 DNS 구역 유지보수가 필수는 아니지만, 다중 도메인을 갖는 사용자의 경우에는 강력히 추천합니다. 


## 보조 DNS 구역 추가
{:#add-a-secondary-dns-zone}

보조 DNS 구역을 추가하려면 아래의 단계를 따르십시오.

* 탐색 메뉴에서 **클래식 인프라**를 선택하여 [{{site.data.keyword.cloud_notm}} 콘솔 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **보조 DNS 구역** 화면으로 이동하십시오.  
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > 보조 구역**을 선택하십시오.
* **구역 추가** 탭을 선택하십시오.
* **구역** 필드에 **구역에 대한 도메인**을 입력하십시오.
* **마스터 이름 서버** 필드에 **마스터 이름 서버의 IP 주소**를 입력하십시오.
* **전송 간격** 필드에서 기본 DNS 구역이 보조 DNS 구역으로 전송할 **전송 시간**(분 단위)을 입력하십시오.
* **추가** 단추를 선택하여 구역을 추가하거나, **취소**를 선택하여 조치를 취소하십시오.

### 추가 이후의 상황
{:#add-a-secondary-dns-zone-next}

보조 DNS 구역은 작성된 후 보조 DNS 구역 화면의 구역 목록에 나타납니다. 기본 구역에서 보조 구역으로의 데이터 전송은 구역이 작성될 때 사용자가 지정한 간격으로 발생합니다. 언제든지 구역을 [편집](#edit-a-secondary-dns-zone), [수동으로 전송](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone) 또는 구역을 기본 구역으로 [변환](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone)할 수 있습니다. 보조 DNS 구역은 또한 언제든지 [삭제](#delete-a-secondary-dns-zone)할 수 있습니다.

## 보조 DNS 구역 편집
{:#edit-a-secondary-dns-zone}

언제든지 마스터 이름 서버 또는 전송 간격을 업데이트하기 위해 보조 DNS 구역을 편집할 수 있습니다. 보조 DNS 구역을 편집하려면 아래 단계를 따르십시오.

* 탐색 메뉴에서 **클래식 인프라**를 선택하여 [{{site.data.keyword.cloud_notm}} 콘솔 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **보조 DNS 구역** 화면으로 이동하십시오.  
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > 보조 구역**을 선택하십시오.
* 편집을 위해 구역을 열려면 **보조 DNS 구역을 포함하는 행**의 어디든 클릭하십시오.
  다중 보조 구역이 있는 경우 보기를 필터링하여 편집이 필요한 구역을 찾을 수 있습니다.
  {:note}  
* **마스터 이름 서버** 및 **전송 간격** 필드를 필요에 따라 업데이트하십시오.
* **업데이트** 단추를 선택하여 보조 DNS 구역을 업데이트하거나, **취소**를 선택하여 조치를 취소하십시오.

### 편집 이후의 상황
{:#edit-a-secondary-dns-zone-next}

보조 DNS 구역을 편집한 후, **마스터 이름 서버** 및 **전송 간격** 값이 업데이트를 반영하며 보조 구역은 새 정보를 바탕으로 전송 수신을 시작합니다. 언제든지 이전 단계를 반복하여 구역을 다시 편집할 수 있습니다.

## 보조 DNS 구역 삭제
{:#delete-a-secondary-dns-zone}

보조 DNS 구역이 작성된 후에는 언제든지 삭제할 수 있습니다. 보조 DNS 구역이 삭제되는 경우 검색할 수 없음을 유의하십시오. 보조 DNS 레코드를 삭제하려면 아래의 단계를 따르십시오.

 * 탐색 메뉴에서 **클래식 인프라**를 선택하여 [{{site.data.keyword.cloud_notm}} 콘솔 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **보조 DNS 구역** 화면으로 이동하십시오.  
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > 보조 구역**을 선택하십시오.
* 삭제가 필요한 구역의 **조치** 드롭 다운 목록에서 **삭제**를 선택하십시오. 팝업 확인 상자가 나타납니다.
  다중 보조 구역이 있는 경우 보기를 필터링하여 삭제할 구역을 찾을 수 있습니다.
  {:note}
* **예** 단추를 선택하여 삭제를 확정하거나, **아니오**를 선택하여 조치를 취소하십시오.

### 삭제 이후의 상황
{:#delete-a-secondary-dns-zone-next}

보조 DNS 구역이 삭제된 후에 기본 구역에서의 자동화된 전송은 중단되고 보조 구역은 더 이상 존재하지 않습니다. 언제든지 기본 구역에 대해 보조 DNS 구역이 필요한 경우 새 [보조 DNS 구역을 작성할 수 있습니다](#add-a-secondary-dns-zone).
