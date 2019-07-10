---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-15"

keywords: Transfer Existing Domain, Transfer multiple domains 

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 도메인 전송
{: #transfer-domains}

## IBM Cloud로 기존 도메인 전송
{:#transfer-an-existing-domain-to-ibm-cloud}

도메인이 등록되면 언제든지 이를 전송할 수 있습니다. 도메인을 서드파티 등록자에서 {{site.data.keyword.cloud}}로 전송하면 도메인 관리 프로세스를 능률화할 수 있습니다. 도메인 전송은 웹 사이트, 이메일 또는 DNS에 영향을 주지 않습니다. 도메인 레코드를 관리하는 등록자만 변경합니다. 기존 도메인을 {{site.data.keyword.cloud_notm}}로 전송하려면 이 문서의 단계를 따르십시오.

## 단일 도메인 전송
{: #transfer-single-domain}

* [{{site.data.keyword.cloud_notm}} 콘솔 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **도메인 등록** 화면으로 이동하십시오. [도메인 등록 화면 액세스](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen)를 참조하십시오.
* **전송** 탭을 선택하십시오.
* **도메인 이름** 필드에 기존 도메인 이름을 입력하십시오.
* **도메인 유형** 드롭 다운 목록에서 도메인 유형을 선택하십시오.
* **등록 시간** 드롭 다운 목록에서 도메인이 활성 상태로 남을 시간을 선택하십시오.

  각 기간의 가격이 시간 옆에 표시되며 도메인이 업데이트될 때 신용카드로 청구되거나 계정의 크레딧에서 차감됩니다.
  {:note}
  
* 도메인을 전송하려면 **계속** 단추를 선택하십시오.

## 여러 도메인 전송
{: #transfer-multiple-domains}

계정에 연결된 활성 신용카드나 계정에 사용 가능한 크레딧이 있는 경우 도메인을 개별적이 아니라 대량으로 {{site.data.keyword.cloud_notm}}로 전송할 수 있습니다. {{site.data.keyword.cloud_notm}}에 대한 다중 도메인을 전송하려면 다음 단계를 수행하십시오.

* [{{site.data.keyword.cloud_notm}} 콘솔 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **도메인 등록** 화면으로 이동하십시오. [도메인 등록 화면 액세스](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen)를 참조하십시오.
* **전송** 탭을 선택하십시오.
* **전송** 탭에서 **다중 도메인 전송** 옵션을 선택하십시오.
* **도메인 이름** 필드에 기존 도메인 이름을 입력하십시오.
* **도메인 유형** 드롭 다운 목록에서 도메인 유형을 선택하십시오.
* **등록 시간** 드롭 다운 목록에서 전송된 도메인이 활성 상태로 남을 시간을 선택하십시오.

각 기간의 가격이 시간 옆에 표시되며 도메인이 업데이트될 때 신용카드로 청구되거나 계정의 크레딧에서 차감됩니다.
{:note}

* 전송할 각각의 추가 도메인에 대해 반복하십시오.

추가 도메인 항목에 대한 추가 공백 필드를 채우려면 **다른 것 추가** 옵션을 선택하십시오. 화면에서 전체 항목을 삭제하려면 **삭제** 아이콘을 선택하십시오.
{:note}

* 도메인을 전송하려면 **계속** 단추를 선택하십시오.



## 다음 작업
{:#transfer-an-existing-domain-to-ibm-cloud-next}

도메인을 전송한 후 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/) 내에서 도메인을 관리할 수 있습니다. 도메인의 등록이 만기 날짜에 가까와지면, **도메인 관리** 화면에서 [갱신](/docs/infrastructure/dns?topic=dns-renew-an-existing-domain)할 수 있습니다.
