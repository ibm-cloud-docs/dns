---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Secondary DNS Zone, Primary Zone, IBM Cloud nameservers

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# 보조 DNS 구역을 기본 구역으로 변환
{:#convert-a-secondary-dns-zone-to-a-primary-zone}

언제든지 [보조 DNS 구역](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone){:new_window}을 기본 구역으로 변환할 수 있습니다. 보조 DNS 구역을 기본으로 변환하면 {{site.data.keyword.BluSoftlayer_notm}} 이름 서버가 변환된 구역에 대한 인증된 이름 서버가 됩니다. 보조 DNS 구역을 기본으로 변환하려면 아래 단계를 따르십시오.

* 탐색 메뉴에서 **클래식 인프라**를 선택하여 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **보조 DNS 구역** 화면으로 이동하십시오. 
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > 보조 구역**을 선택하십시오.
* 원하는 보조 구역에 대한 **조치** 드롭 다운 목록에서 **기본으로 변환**을 선택하십시오.
* **예** 단추를 선택하여 구역을 변환하거나, **아니오**를 선택하여 조치를 취소하십시오.

## 다음 작업
{:#convert-a-secondary-dns-zone-to-a-primary-zone-next}

보조 DNS 구역을 기본으로 변환한 후 **전달 구역** 화면에서 이를 볼 수 있습니다. 이전에 구역에 대해 존재했던 모든 SOA 및 NS 레코드가 {{site.data.keyword.BluSoftlayer_notm}} SOA 및 NS 레코드로 대체되며, 이들은 편집할 수 없습니다. 여전히 [나머지 구역 레코드를 편집](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record)할 수 있습니다.
