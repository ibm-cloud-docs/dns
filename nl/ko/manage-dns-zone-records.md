---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone Record, Update DNS Zone Record, edit dns zone record, add dns zone record, delete dns zone record 

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

# DNS 구역 레코드 관리
{: #manage-dns-zone-records}
이 절에서는 DNS 구역 레코드를 추가, 편집 및 삭제하는 방법을 자세히 설명합니다. 

## DNS 구역 레코드 추가
{: #add-a-dns-zone-record}

[DNS 구역을 추가](/docs/infrastructure/dns?topic=dns-manage-dns-zones#add-a-dns-zone)한 후, 언제든지 구역에 레코드를 추가할 수 있습니다. 이러한 레코드는 다음과 같습니다.

* A(호스트) 레코드
* AAAA(호스트) 레코드
* CNAME(별명) 레코드
* MX(메일 교환) 레코드
* TXT(텍스트) 레코드
* SRV(서비스) 레코드

DNS 구역 레코드를 추가하려면 아래의 단계를 따르십시오.

* **DNS 구역** 화면으로 이동하십시오. [DNS 구역 화면 사용](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)을 참조하십시오.
* 레코드가 추가될 DNS 구역을 선택하십시오.
* **리소스 유형** 드롭 다운 목록에서 원하는 **리소스 유형**을 선택하십시오.
* 새 레코드에 대한 나머지 필드를 완료하십시오. 자세한 정보는 아래의 표를 참조하십시오. <br/><br/><table border="1"><tbody><tr><th scope="col">레코드 유형</th><th scope="col">필드</th><th scope="col">입력 항목</th></tr><tr><td rowspan="3">A(호스트), AAAA(호스트) 또는 CNAME(별명)</td><td>호스트</td><td><strong>호스트 이름</strong>을 입력하십시오.</td></tr><tr><td>지정 대상</td><td>호스트 레코드가 가리키는 <strong>IP 주소</strong>를 입력하십시오.</td></tr><tr><td>TTL</td><td>드롭 다운 목록에서 TTL(Time to Live)을 선택하십시오. TTL 기본값은 15분입니다.</td></tr><tr><td rowspan="4">MX(메일 교환)</td><td>우선순위</td><td>대상 호스트의 <strong>우선순위</strong>를 입력하십시오. 숫자가 낮을수록, 우선순위가 더 높습니다.</td></tr><tr><td>호스트</td><td><strong>호스트 이름</strong>을 입력하십시오.</td></tr><tr><td>이동</td><td>메일 서버의 <strong>CNAME</strong>을 입력하십시오. 이는 일반적으로 `mail.example.com`으로 표시됩니다. </td></tr><tr><td>TTL</td><td>드롭 다운 목록에서 TTL(Time to Live)을 선택하십시오. TTL 기본값은 15분입니다.</td></tr><tr><td rowspan="3">TXT(텍스트)</td><td>이름</td><td><strong>@</strong> 또는 <strong>도메인 이름</strong>을 입력하십시오.</td></tr><tr><td>값</td><td>도메인 또는 IP의 적절한 이메일 종료 권한을 확인하려면 <strong>레코드</strong>를 입력하십시오.</td></tr><tr><td>TTL</td><td>드롭 다운 목록에서 TTL(Time to Live)을 선택하십시오. TTL 기본값은 15분입니다.</td></tr><tr><td rowspan="8">SRV(서비스 레코드)</td><td>서비스</td><td>원하는 서비스의 <strong>기호 이름</strong>을 입력하십시오.</td></tr><tr><td>프로토콜</td><td>드롭 다운 목록에서 사용될 <strong>프로토콜</strong>을 선택하십시오.</td></tr><tr><td>우선순위</td><td>대상 호스트의 <strong>우선순위</strong>를 입력하십시오. 숫자가 낮을수록, 우선순위가 더 높습니다.</td></tr><tr><td>가중치</td><td>동일한 우선순위를 갖는 레코드에 대한 <strong>상대 가중치</strong>를 입력하십시오.</td></tr><tr><td>포트</td><td>서비스가 발견될 <strong>TCP 또는 UPD 포트</strong>를 입력하십시오.</td></tr><tr><td>호스트(선택사항)</td><td>서비스의 <strong>호스트 이름</strong>을 입력하십시오.</td></tr><tr><td>대상</td><td>서비스를 제공하는 머신의 <strong>명목 호스트 이름</strong>을 입력하십시오.</td></tr><tr><td>TTL</td><td>드롭 다운 목록에서 TTL(Time to Live)을 선택하십시오. TTL 기본값은 15분입니다.</td></tr></tbody></table><br/>
* **레코드 추가** 단추를 선택하여 새 구역 레코드를 추가하십시오.

### 다음 작업
{:#add-a-dns-zone-record-next}

구역 레코드를 추가한 후 해당 레코드가 화면의 **기존 레코드** 섹션에 나타납니다. 언제든지 구역 레코드를 [편집](#edit-a-dns-zone-record) 또는 [삭제](#delete-a-dns-zone-record)할 수 있습니다.

## DNS 구역 레코드 편집
{: #edit-a-dns-zone-record}

TTL(Time to Live), 포인터(PTR) 레코드 및 호스트 이름 같은 다양한 영역을 업데이트하기 위해 사용자가 기존 DNS 구역 레코드를 편집할 수 있습니다. 언제든지 여러 호스트와 별명을 DNS 구역 레코드와 연관시킬 수 있습니다. 기존 DNS 구역 레코드를 편집하려면 아래의 단계를 따르십시오.

* 탐색 메뉴에서 **클래식 인프라**를 선택하여 원하는 **DNS 구역** 화면으로 이동하십시오. 
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > 전달 구역**을 선택하십시오.
* 임의의 기존 레코드를 포함하는 **행**을 클릭하십시오. 

  이탤릭체의 레코드는 편집할 수 없습니다. 이는 일반적으로 NS(이름 서버) 레코드로 제한됩니다.
  {: note}
  
* 필요에 따라 레코드의 세부사항을 업데이트하십시오.
* **업데이트** 단추를 선택하여 레코드를 업데이트하거나, **취소**를 선택하여 조치를 취소하십시오.

### 다음 작업
{: #edit-a-dns-zone-record-next}

레코드를 업데이트하면 해당 세부사항이 자동으로 새 항목을 표시합니다. 레코드는 언제든지 업데이트될 수 있고, 기존 레코드가 삭제될 수 있으며, 새 레코드가 [추가](#add-a-dns-zone-record)될 수 있습니다.

## DNS 구역 레코드 삭제
{: #delete-a-dns-zone-record}

DNS 구역 레코드는 **DNS 구역 편집** 화면을 통해 삭제됩니다. DNS 구역 레코드 삭제는 되돌릴 수 없습니다.
* DNS 구역의 목록에서 이름을 클릭하여 삭제할 레코드가 있는 DNS 구역을 선택하십시오. 
* 원하는 레코드가 포함된 행의 끝에서 삭제 아이콘을 선택하십시오. 팝업 확인 상자가 나타납니다.
* **예** 단추를 선택하여 삭제를 확정하거나, **아니오**를 선택하여 조치를 취소하십시오.
