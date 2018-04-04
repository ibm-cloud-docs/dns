---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-01"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Cpanel/WHM에서 사용자 고유의 이름 서버 작성

이 문서는 웹 호스트 관리자(WHM)를 사용하여 사용자 고유의 이름 서버를 작성하는 방법에 대한 단계를 제공합니다. 이들 단계를 수행한 후 문제가 발생하는 경우 이 문서를 참조하는 지원 티켓을 제출하십시오. 

1. 먼저, 이름 서버의 이름을 결정하십시오. 예를 들어, 호스팅 회사가 “Awesome Server Hosting”이라고 하면 `ns1.awesomeserverhosting.com` 및 `ns2.awesomeserverhosting.com`으로 설정하려고 합니다. 

* 브라우저에서 https://XX.XX.XX.XX:2087 로 이동하여 서버의 WHM에 로그인하십시오. 

* 이름 서버를 설정하려면 왼쪽 막대의 첫 번째 옵션을 선택하십시오. “기본 cPanel/WHM 설정”입니다.  

 * 여기에서 기본, 2차, 3차 및 4차 이름 서버의 이름을 설정할 수 있습니다. 

 * 완료했으면 “저장” 단추를 선택하십시오. 

2. 이제 내 서버에 “awesomeserverhosting.com”에 대한 구역 파일을 작성하십시오. 이 태스크를 수행하는 두 가지 방법이 있습니다. 

첫 번째 방법: “awesomeserverhosting.com”에 대한 도메인 계정을 작성하십시오. 이에 대한 지시사항은 이 문서의 범위를 벗어납니다. 자세한 정보는 [cPanel 문서](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)를 참조하십시오.  

   * 왼쪽 사이드바의 “DNS 기능” 아래에서 “DNS 구역 추가”를 선택하십시오. 

   * “awesomeserverhosting.com”에 대해 기본 웹 사이트가 호스팅되는 IP 주소 및 도메인 이름을 제공하십시오. 

   **참고: 이 서버에 `awesomeserverhosting.com`을 호스팅할 계획이 아닌 경우에만 이를 수행하십시오!**

   * **네트워킹 설정** 표제 아래에서 **이름 서버 IP**를 클릭하십시오. 

   * 이름 서버의 이름을 제공하십시오. 예를 들어, `ns1.awesomeserverhosting.com`을 제출한 후 `ns2.awesomeserverhosting.com`을 제출하십시오. 

   * 왼쪽 막대에서, **서비스 구성** 아래의 **이름 서버 설정**을 찾으십시오. 

   * 다음과 비슷한 메시지가 표시됩니다. “사용할 예정이 아니면 이름 서버를 사용으로 설정하지 않는 것이 좋습니다. 이름 서버를 사용 안함으로 설정하려면 항상 서비스 관리자에서 이름 서버를 끌 수 있습니다”.

   * 이름 서버를 시작하고 실행 중이므로, **계속 >>**이라는 단추를 선택하십시오. `cPanel` 도구는 서버에 적절한 패키지가 설치되었고 패키지가 제대로 작업하여 이름 서비스를 호스팅하도록 구성되게 합니다. 이제 모두 설정되었습니다! 

외부 링크:

* [cPanel 문서](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
