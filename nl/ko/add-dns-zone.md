---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS 구역 추가

{{site.data.keyword.BluSoftlayer_notm}}에 의한 DNS 관리는 {{site.data.keyword.BluSoftlayer_notm}} 네트워크 상에 없을 수도 있는 DNS 구역으로 확장합니다. 자사의 인터페이스를 사용하면 언제든지 DNS 구역을 단일 도메인으로 또는 대량으로 추가할 수 있습니다. DNS 구역의 추가는 현재 고객 포털의 [제어](https://control.softlayer.com/) 버전에서 발생합니다. 하나 이상의 DNS 구역을 추가하려면 아래의 단계를 따르십시오. 

* 고유한 신임 정보를 사용하여 고객 포털의 [제어](https://control.softlayer.com/) 버전에 로그인하십시오. 
* **네트워크** 드롭 다운 메뉴에서 **DNS**를 선택하십시오. 
* **전달 구역**을 선택하십시오. 
* 맨 위 오른쪽의 **DNS 구역 추가** 탭을 선택하십시오. 
* 단일 도메인 또는 다중 도메인을 추가 중인지 여부를 판별하십시오. <br> <br><table border="1"><tbody><tr><th>추가할 도메인</th><th>수행할 작업</th></tr><tr><td>단일 도메인</td><td>화면의 <strong>단일 도메인 추가</strong> 섹션에서 다음 단계를 완료하십시오. <br> <ul><li><strong>도메인 이름</strong> 필드에 <strong>도메인 이름</strong>을 입력하십시오. </li><li><strong>IP 주소</strong> 필드에 도메인 이름이 가리킬 <strong>IP 주소</strong>를 입력하십시오. </li><li><strong>구역 추가</strong> 단추를 클릭하여 도메인을 추가하십시오. <br> </li></ul></td></tr><tr><td>다중 도메인</td><td>도메인이 단일 IP 주소 또는 다중 IP 주소와 연관되는지 여부를 판별하십시오. <br> <p> </p><p> </p><p> </p><p> </p><ul><li>도메인이 단일 IP 주소와 연관되는 경우, <ul><li><strong>도메인</strong> 텍스트 상자에 <strong>각 도메인</strong>을 입력하십시오. </li><li><strong>기본 IP 주소</strong> 필드에 <strong>IP 주소</strong>를 입력하십시오. </li><li><strong>구역 추가</strong> 단추를 클릭하여 도메인을 대량으로 추가하십시오. </li></ul></li><li>도메인이 다중 IP 주소와 연관되는 경우, <ul><li><strong>도메인</strong> 텍스트 상자에 <strong>각 도메인</strong> 및 그의 대응하는 <strong>IP 주소</strong>를 단일 행 항목으로 입력하십시오. </li><li><strong>구역 추가</strong> 단추를 클릭하여 도메인을 대량으로 추가하십시오. </li></ul></li><li> </li></ul></td></tr></tbody></table>

## 다음 작업

DNS 구역을 추가한 후 해당 DNS 구역이 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/) 내의 [DNS 구역 화면](access-dns-zones-screen.html)의 DNS 구역 목록에 나타납니다. 구역은 언제든지 [편집](edit-dns-zone-record.html) 또는 [삭제](delete-dns-zone.html)될 수 있습니다. 
