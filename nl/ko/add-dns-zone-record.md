---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS 구역 레코드 추가

[DNS 구역을 추가](add-dns-zone.html)한 후, 언제든지 구역에 레코드를 추가할 수 있습니다. 이러한 레코드는 다음과 같습니다. 

* A(호스트) 레코드
* AAAA(호스트) 레코드
* CNAME(별명) 레코드
* MX(메일 교환) 레코드
* TXT(텍스트) 레코드
* SRV(서비스) 레코드

DNS 구역 레코드를 추가하려면 아래의 단계를 따르십시오. 

* 원하는 **DNS 구역** 화면으로 이동하십시오. [DNS 구역 화면 사용](use-dns-zones-screen.html)을 참조하십시오. 
* 레코드가 추가될 DNS 구역을 선택하십시오. 
* **리소스 유형** 드롭 다운 목록에서 원하는 **리소스 유형**을 선택하십시오. 
* 새 레코드에 대한 나머지 필드를 완료하십시오. 자세한 정보는 아래 표를 참조하십시오. <br/><br/><table border="1"><tbody><tr><th>레코드 유형</th><th>필드</th><th>입력 항목</th></tr><tr><td rowspan="3">A(호스트), AAAA(호스트) 또는 CNAME(별명)</td><td>호스트</td><td><strong>호스트 이름</strong>을 입력하십시오. </td></tr><tr><td>지정 대상</td><td>호스트 레코드가 가리키는 <strong>IP 주소</strong>를 입력하십시오. </td></tr><tr><td>TTL</td><td>드롭 다운 목록에서 TTL(Time to Live)을 선택하십시오. TTL 기본값은 15분입니다. </td></tr><tr><td rowspan="4">MX(메일 교환)</td><td>우선순위</td><td>대상 호스트의 <strong>우선순위</strong>를 입력하십시오. 숫자가 낮을수록, 우선순위가 더 높습니다. </td></tr><tr><td>호스트</td><td><strong>호스트 이름</strong>을 입력하십시오. </td></tr><tr><td>이동</td><td>메일 서버의 <strong>CNAME</strong>을 입력하십시오. 이것은 대개 mail.example.com으로 표시됩니다. </td></tr><tr><td>TTL</td><td>드롭 다운 목록에서 TTL(Time to Live)을 선택하십시오. TTL 기본값은 15분입니다. </td></tr><tr><td rowspan="3">TXT(텍스트)</td><td>이름</td><td><strong>@</strong> 또는 <strong>도메인 이름</strong>을 입력하십시오. </td></tr><tr><td>값</td><td>도메인 또는 IP의 적절한 이메일 종료 권한을 확인하려면 <strong>레코드</strong>를 입력하십시오. </td></tr><tr><td>TTL</td><td>드롭 다운 목록에서 TTL(Time to Live)을 선택하십시오. TTL 기본값은 15분입니다. </td></tr><tr><td rowspan="8">SRV(서비스 레코드)</td><td>서비스</td><td>원하는 서비스의 <strong>기호 이름</strong>을 입력하십시오. </td></tr><tr><td>프로토콜</td><td>드롭 다운 목록에서 사용될 <strong>프로토콜</strong>을 선택하십시오. </td></tr><tr><td>우선순위</td><td>대상 호스트의 <strong>우선순위</strong>를 입력하십시오. 숫자가 낮을수록, 우선순위가 더 높습니다. </td></tr><tr><td>가중치</td><td>동일한 우선순위를 갖는 레코드에 대한 <strong>상대 가중치</strong>를 입력하십시오. </td></tr><tr><td>포트</td><td>서비스가 발견될 <strong>TCP 또는 UPD 포트</strong>를 입력하십시오. </td></tr><tr><td>호스트(선택사항)</td><td>서비스의 <strong>호스트 이름</strong>을 입력하십시오. </td></tr><tr><td>대상</td><td>서비스를 제공하는 머신의 <strong>명목 호스트 이름</strong>을 입력하십시오. </td></tr><tr><td>TTL</td><td>드롭 다운 목록에서 TTL(Time to Live)을 선택하십시오. TTL 기본값은 15분입니다. </td></tr></tbody></table><br/>
* **레코드 추가** 단추를 선택하여 새 구역 레코드를 추가하십시오. 

## 다음 작업

구역 레코드를 추가한 후 해당 레코드가 화면의 **기존 레코드** 섹션에 나타납니다. 언제든지 구역 레코드를 [편집](edit-dns-zone-record.html) 또는 삭제할 수 있습니다. 
