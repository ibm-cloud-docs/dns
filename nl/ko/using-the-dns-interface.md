---
copyright:
  years: 1994, 2017-2019
lastupdated: "2019-02-01"

subcollection: dns

keywords: DNS interface, new records, Add DNS Zone button

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS 인터페이스 사용 방법
{:#how-to-use-the-dns-interface}

IBM Cloud 고객 포털을 통해 DNS 인터페이스를 이용하려면 다음 단계를 수행하십시오.

* [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)로 이동하십시오.
* 탐색 메뉴에서 **클래식 인프라**를 선택하십시오.
* **네트워크->DNS->전달 구역**을 선택하십시오.
* 관리하려는 도메인을 선택하거나, 페이지 오른쪽에 있는 **DNS 구역 추가** 단추를 선택하십시오.

## DNS 인터페이스 개요
{:#dns-interface-overview}
고객 포털의 DNS 인터페이스에서 작업하면 DNS의 모든 측면을 관리할 수 있습니다. 화면 맨 위에 있는 정적 메뉴 표시줄을 사용하여 인터페이스에 있는 임의의 화면에서 모든 유형의 DNS 관리를 수행할 수 있습니다.

## DNS 관리
{:#manage-dns}
포털의 DNS 인터페이스에 접근할 때 **DNS 관리** 화면으로 직접 라우트되는데, 여기에서 사용자 계정과 연관된 모든 기존 기본 DNS를 보기, 편집 또는 삭제할 수 있습니다.

* 새 레코드를 추가하려면 단순히 **새 레코드 추가** 아래에 제공되는 필드를 완성한 후 **레코드 추가** 단추를 클릭하십시오.
* 기존 레코드를 수정하려면 해당 레코드를 포함하는 행을 클릭하십시오. 레코드가 **편집** 모드로 변환됩니다. 설정을 원하는 값으로 변경하고 **업데이트**를 클릭하십시오.
* 레코드를 삭제하려면 레코드 오른쪽에 있는 빨간색 원을 선택한 후 프롬프트에서 **예**를 클릭하십시오.

## 보조 DNS
{:#secondary-dns}

* [고객 포털 클래식 인프라 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)로 이동하십시오.
* 탐색 메뉴에서 **클래식 인프라**를 선택하십시오.
* **네트워크->DNS->보조 구역**을 선택하십시오.

이 화면에서 보조 DNS 설정을 추가 또는 수정할 수 있습니다.

* 새 레코드를 추가하려면 **구역 추가**를 선택하고, 필드를 채운 후 **추가**를 선택하십시오.
* 보조 DNS 레코드를 제거하거나 기본 레코드로 변환하려면 페이지 오른쪽의 **조치** 드롭 다운을 사용하고 적절한 옵션을 선택하십시오.

## 역방향 DNS
{:#reverse-dns}

포털 탐색을 통해 DNS 인터페이스를 이용하려면 다음 단계를 수행하십시오.

* [고객 포털 클래식 인프라 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)로 이동하십시오.
* 탐색 메뉴에서 **클래식 인프라**를 선택하십시오.
* **네트워크->DNS->역방향 레코드**를 선택하십시오.
* 드롭 다운 메뉴에서, 역방향 DNS를 변경하려는 IP 주소를 선택하거나 입력한 후 **IP 보기**를 선택하십시오.
  * 레코드를 추가하려면 역방향 DNS 항목에 사용하려는 호스트 이름을 입력하십시오.
  * 레코드에 대한 TTL(Time to Live)을 설정하십시오.
  * 정보를 확인한 후 **저장**을 선택하십시오.

페이지 오른쪽의 **이 서브넷의 모든 IP에 대해 RDNS 편집**을 클릭하여 전체 서브넷을 수정할 수 있습니다.

* 이 페이지에서 업데이트하려는 IP에 대한 행을 선택하십시오.
* 필드에 정보를 입력한 후 **업데이트**를 선택하십시오. "참고" 필드는 선택사항입니다.

<!--## Propagation Check

* Navigate to the [Customer Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/).
* Select **Network > Tools**

On the page that loads, you can select from multiple tools; To check the propagation of your domain name through the DNS servers, use the bottom option.

* Enter the appropriate information into the fields, then select **Check DNS**
* After a few moments, the box to the right will update with the current DNS information for the domain.-->
