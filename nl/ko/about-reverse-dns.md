---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Reverse DNS 

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 역방향 DNS 정보
{:#about-reverse-dns}

역방향 DNS는 DNS(Domain Name System)가 도메인 이름을 연관된 IP 주소로 해석하는 것처럼 IP 주소를 도메인 이름으로 해석하는 방법입니다. 역방향 DNS의 한 가지 적용은 스팸 필터로서입니다. 일반적으로, 스팸 발송자는 도메인 이름과 일치하지 않는 올바르지 않은 IP 주소를 사용합니다. 역방향 DNS 검색 프로그램은 수신 메시지의 IP 주소를 DNS 데이터베이스에 입력합니다. IP 주소와 일치하는 올바른 이름을 찾지 못하는 경우 서버는 해당 메시지를 차단합니다. 역방향 DNS는 네트워크 문제점 해결 호출(예: `ping`) 같은 작업과 네트워크 모니터링 도구에도 사용됩니다.
