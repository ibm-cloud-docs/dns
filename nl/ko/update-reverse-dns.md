---
copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-02-26"

keywords: Reverse DNS Record, Reverse DNS, IP address, Individual IP Select

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 역방향 DNS 레코드 업데이트
{:#update-reverse-dns-record}

역방향 DNS를 사용하면 IP 주소와 연관된 도메인을 식별할 수 있습니다. 고객은 언제든지 자신의 역방향 DNS를 업데이트하여 PTR 및 TTL(Time to Live)을 변경할 수 있습니다. **관리** 버전 [IBM Cloud Console ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/) 내에서, **검색 및 대체** 도구를 사용하여 PTR 레코드를 대량으로 업데이트할 수 있습니다. 이 도구를 사용하면 검색 필드에 PTR의 일부 또는 전체 PTR을 입력하고 대응하는 PTR 내의 모든 발생을 원하는 정보로 대체할 수 있습니다. 

이 도구는 기존 PTR이 서버 또는 VLAN과 연관될 때만 작동함을 주의하십시오. PTR이 없으면 세부사항이 나열되지 않으며 업데이트 시도는 오류가 됩니다. 

역방향 DNS PTR 레코드를 추가하려면 [PTR(포인터) 레코드 추가 및 편집](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record)을 참조하십시오. 역방향 DNS 레코드를 업데이트하려면 다음 단계를 수행하십시오.

 * 고유한 인증 정보를 사용하여 [IBM Cloud Console ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)로 이동하십시오.
 * 탐색 메뉴에서 **클래식 인프라**를 선택하십시오.
 * 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > DNS 되돌리기**를 선택하십시오.
 * IP 주소를 입력하거나 드롭 다운 메뉴에서 선택하고 **IP 보기**를 클릭하십시오.
 * 나열된 옵션을 편집하고 **저장**을 클릭하십시오. 전체 서브넷을 변경하도록 **이 서브넷에 있는 모든 IP의 RDNS 편집**도 선택할 수 있습니다. 
 

