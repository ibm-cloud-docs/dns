---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS 구역 관리
{: #manage-dns-zones}

## DNS 구역 추가
{: #add-a-dns-zone}

{{site.data.keyword.cloud}}에 의한 DNS 관리는 {{site.data.keyword.cloud_notm}} 네트워크 상에 없을 수도 있는 DNS 구역으로 확장합니다. 자사의 인터페이스를 사용하면 언제든지 DNS 구역을 단일 도메인으로 또는 대량으로 추가할 수 있습니다. DNS 구역 추가는 현재 [IBM Cloud 콘솔](https://{DomainName}/)에서 발생합니다. 하나 이상의 DNS 구역을 추가하려면 아래의 단계를 따르십시오.

* 고유 인증 정보를 사용하여 [IBM Cloud 콘솔](https://{DomainName}/)에 로그인하십시오.
* 탐색 메뉴에서 **클래식 인프라**를 선택하십시오.
* **네트워크** 드롭 다운 메뉴에서 **DNS**를 선택하십시오.
* **전달 구역**을 선택하십시오.
* 맨 위 오른쪽의 **DNS 구역 추가** 탭을 선택하십시오.
* 단일 도메인 또는 다중 도메인을 추가 중인지 여부를 판별하십시오.

|추가할 도메인|수행할 작업|
|---|---|
|단일 도메인|화면의 **단일 도메인 추가** 섹션에서 다음 단계를 완료하십시오. <ul><li>**도메인 이름** 필드에 **도메인 이름**을 입력하십시오.</li><li>**IP 주소** 필드에 도메인 이름이 가리킬 **IP 주소**를 입력하십시오.</li><li>**구역 추가** 단추를 클릭하여 도메인을 추가하십시오.</li></ul>|
|다중 도메인|도메인이 단일 IP 주소 또는 다중 IP 주소와 연관되는지 여부를 판별하십시오. <ul><li>도메인이 단일 IP 주소와 연관되는 경우, <ul><li>**도메인** 텍스트 상자에 **각 도메인**을 입력하십시오.</li><li>**기본 IP 주소** 필드에 **IP 주소**를 입력하십시오.</li><li>**구역 추가** 단추를 클릭하여 도메인을 대량으로 추가하십시오.</li></ul></li><li>도메인이 다중 IP 주소와 연관되는 경우, <ul><li>**도메인** 텍스트 상자에 **각 도메인** 및 이에 대응되는 **IP 주소**를 단일 행 항목으로 입력하십시오.</li><li>**구역 추가** 단추를 클릭하여 도메인을 대량으로 추가하십시오.</li></ul></li></ul>


### 다음 작업
{:#add-a-dns-zone-next}

단일 구역 추가가 완료되면 자동으로 구역 편집 페이지로 경로 재지정됩니다.
새 DNS 구역은 [IBM Cloud 콘솔 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/) 내의 [DNS 구역 화면](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)에서 DNS 구역의 목록에 나타납니다. 구역은 언제든지 [편집](#edit-a-dns-zone) 또는 [삭제](#delete-a-dns-zone)될 수 있습니다.

## DNS 구역 편집
{: edit-a-dns-zone}
구역 이름을 클릭하여 DNS 구역 화면의 구역 목록에서 편집할 DNS 구역을 선택하십시오. DNS 구역 편집 페이지가 열립니다. 여기서 DNS 구역을 변경하고 **SOA 업데이트**를 클릭하여 변경사항을 커미트할 수 있습니다. 

**DNS 구역 편집** 화면을 사용하면 편집 중인 구역의 기존 레코드를 편집하고 새 레코드를 추가할 수 있습니다. 이 화면에서 구역을 내보내거나 삭제할 수도 있습니다.

### 다음 작업
{:#edit-a-dns-zone-next}

**모든 DNS 구역 보기**를 클릭하여 DNS 구역의 목록으로 돌아가십시오.


## DNS 구역 삭제
{: #delete-a-dns-zone}

DNS 구역이 추가된 후 언제든지 삭제할 수 있습니다. DNS 구역 삭제는 영구적입니다. 실행 취소할 수 없습니다. DNS 구역을 삭제하려면 다음 단계를 수행하십시오.

* 탐색 메뉴에서 **클래식 인프라**를 선택하여 원하는 **DNS 구역** 화면으로 이동하십시오. 
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS**를 선택하고 필요한 구역의 유형을 선택하십시오.
* 원하는 DNS 구역을 포함하는 행의 끝에서 **삭제** 아이콘을 선택하십시오. 팝업 확인 상자가 나타납니다.
* **예** 단추를 선택하여 삭제를 확정하거나, **아니오**를 선택하여 조치를 취소하십시오.

DNS 구역 편집 화면에서 구역을 삭제할 수도 있습니다.
{:tip}

### 다음 작업
{:#delete-a-dns-zone-next}

DNS 구역을 삭제하면 더 이상 [IBM Cloud 콘솔 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)을 사용하여 이를 관리할 수 없습니다. 다시 대시보드에서 삭제된 구역을 관리하려면 이를 [새 구역으로 추가](#add-a-dns-zone)해야 합니다.
