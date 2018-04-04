---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 역방향 DNS 레코드 업데이트

역방향 DNS를 사용하면 IP 주소와 연관된 도메인을 식별할 수 있습니다. 고객은 언제든지 자신의 역방향 DNS를 업데이트하여 PTR 및 TTL(Time to Live)을 변경할 수 있습니다. **관리** 버전 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/) 내에서, **검색 및 대체** 도구를 사용하여 PTR 레코드를 대량으로 업데이트할 수 있습니다. 이 도구를 사용하면 검색 필드에 PTR의 일부 또는 전체 PTR을 입력하고 대응하는 PTR 내의 모든 발생을 원하는 정보로 대체할 수 있습니다.  

이 도구는 기존 PTR이 서버 또는 VLAN과 연관될 때만 작동함을 주의하십시오. PTR이 없으면 세부사항이 나열되지 않으며 업데이트 시도는 오류가 됩니다.  

역방향 DNS PTR 레코드를 추가하려면 [PTR(포인터) 레코드 추가 및 편집](add-and-edit-ptr-pointer-record.html)을 참조하십시오. 역방향 DNS 레코드를 업데이트하려면 다음 단계를 수행하십시오. 

 * 고유한 신임 정보를 사용하여 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/)로 이동하십시오. 
 * **네트워크** 드롭 다운 메뉴에서 **DNS**를 선택하십시오. 
 * **역방향 DNS** 메뉴 옵션을 선택하십시오. 
 * 업데이트가 모든 대응하는 IP 주소 네트워크 VLAN에 작성되어야 하는지 아니면 개별 IP를 변경해야 하는지 여부를 판별하십시오. <br><br><table border="1"><tbody><tr><th>업데이트 작성 범위</th><th>수행할 작업</th></tr><tr><td>개별 IP</td><td><ul><li><b>드롭 다운 메뉴</b>를 선택하여 IP 주소를 보십시오. </li><li>서버와 연관된 역방향 DNS 세부사항을 보려면 <strong>IP 주소</strong>를 클릭하십시오. </li></ul></td></tr><tr><td>네트워크 VLAN의 모든 대응하는 IP 주소</td><td><ul><li>위에서 설명한 대로 IP를 선택한 후 <strong>IP 보기</strong> 옵션을 선택하십시오. </li><li><strong>이 서브넷의 모든 IP에 대한 RDNS 편집</strong> 옵션을 선택하십시오. </li></ul></td></tr></tbody></table><br/>
 * 개별 IP의 경우 단순히 **호스트 이름** 및 **역방향 TTL**을 추가한 후 **저장**을 선택하십시오. 전체 **서브넷**에 대해서는 **역방향 DNS** 열 아래의 열린 공간을 강조표시하고 **호스트 이름**을 추가한 후 **업데이트** 단추를 선택하십시오. 이 태스크는 서브넷의 모든 IP 주소에 대해 수행되어야 합니다. 
