---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Disable Recursion, DNS IBM Cloud DNS servers, BIND configuration file

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# DNS의 순환 사용 안함
{:#disable-recursion-for-dns}

IBM Cloud DNS 서버는 기본적으로 순환(recursion)을 수행합니다. 순환은 DNS 서버가 도메인 자체를 해석할 수 없을 때 도메인 이름 해석을 돕기 위해 다른 DNS 서버에 접속할 수 있게 합니다. 순환은 필요할 때 유용한 도구임을 증명할 수 있지만, DNS 서버를 열어 공격에 노출되면 DNS 서버를 완전히 작동 중지시킬 수 있습니다. 시스템 관리자는 일반적으로 순환의 필요성을 확인하고 그에 따라 조치를 취합니다. 그렇지 않으면, 순환을 사용하지 않는 것이 가장 좋습니다. DNS 순환을 사용 안함으로 설정하려면 운영 체제나 제어판에 따라서 아래 단계를 따르십시오.

## Plesk에서 순환 사용 안함
{:#disable-recursion-in-plesk}
* **Plesk 관리 패널**에 로그인하십시오.
* **도구 및 설정**을 선택하십시오.
* 섹션에서 **DNS 템플리트 설정**을 클릭하십시오.
* **DNS 순환** 섹션에서 **Localnets**를 선택하십시오.
* **확인** 단추를 클릭하십시오.

## Windows Server 2003 및 2008에서 순환 사용 안함
{:#disable-recursion-in-windows-server}

* **시작** 메뉴에서 **DNS 관리자**를 사용하십시오.
  * **시작** 단추를 클릭하십시오.
  * **관리 도구**를 선택하십시오.
  * **DNS**를 선택하십시오.
* **콘솔 트리**에서 원하는 **DNS 서버**를 마우스 오른쪽 단추로 클릭하십시오.
* **특성** 탭을 선택하십시오.
* **서버 옵션** 섹션에서 **고급** 단추를 클릭하십시오.
* **순환 사용 안함** 선택란을 선택하십시오.
* **확인** 단추를 클릭하십시오.

## Linux에서 순환 사용 안함
{:#disable-recursion-in-linux}

 * 운영 체제 내에서 BIND 구성 파일을 찾으십시오. BIND 구성 파일은 대개 다음 경로 중 하나에 위치합니다.
  * /etc/bind/named.conf
  * /etc/named.conf
* 원하는 편집기에서 named.conf 파일을 여십시오.
* **옵션** 섹션에 다음 세부사항을 추가하십시오. <br/>`allow-transfer {"none";};`<br/>`allow-recursion {"none";};`<br/>`recursion no;`
* 디바이스를 다시 시작하십시오.
