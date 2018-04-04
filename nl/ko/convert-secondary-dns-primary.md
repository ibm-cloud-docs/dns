---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 보조 DNS 구역을 기본 구역으로 변환

언제든지 [보조 DNS 구역](add-secondary-dns-zone.html){:new_window}을 기본 구역으로 변환할 수 있습니다. 보조 DNS 구역을 기본으로 변환하면 {{site.data.keyword.BluSoftlayer_notm}} 이름 서버가 변환된 구역에 대한 인증된 이름 서버가 됩니다. 보조 DNS 구역을 기본으로 변환하려면 아래 단계를 따르십시오. 

* [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/)의 **보조 DNS 구역** 화면으로 이동하십시오. [DNS 구역 화면 사용](use-dns-zones-screen.html){:new_window}을 참조하십시오. 
* 원하는 보조 구역에 대한 **조치** 드롭 다운 목록에서 **기본으로 변환**을 선택하십시오. 
* **예** 단추를 선택하여 구역을 변환하거나, **아니오**를 선택하여 조치를 취소하십시오. 

## 다음 작업

보조 DNS 구역을 기본으로 변환한 후 **전달 구역** 화면에서 이를 볼 수 있습니다. 이전에 구역에 대해 존재했던 모든 SOA 및 NS 레코드가 {{site.data.keyword.BluSoftlayer_notm}} SOA 및 NS 레코드로 대체되며, 이들은 편집할 수 없습니다. 여전히 [나머지 구역 레코드를 편집](edit-dns-zone-record.html)할 수 있습니다. 
