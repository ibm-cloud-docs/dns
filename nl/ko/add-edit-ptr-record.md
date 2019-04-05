---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Record PTR, IP addresses, Reverse DNS feature

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# PTR(포인터) 레코드 추가 또는 편집
{:#add-or-edit-a-ptr-pointer-record}

PTR 또는 포인터 레코드는 IP 주소를 호스트 이름으로 해석합니다. 사용자는 [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/){:new_window}의 역방향 DNS 기능을 사용하여 IP 주소와 연관될 PTR 레코드를 추가할 수 있습니다. 또한, PTR 레코드는 추가된 것과 같은 방법으로 편집할 수 있습니다. 디바이스에 대한 PTR 레코드를 추가 또는 편집하려면 아래의 단계를 따르십시오.

* **디바이스 목록**에서 PTR 레코드를 수신할 디바이스에 대한 **공인 IP 주소**를 검색하십시오.
* 탐색 메뉴에서 클래식 인프라**를 선택하여 **[고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/) by selecting **에서 **DNS 레코드 되돌리기** 화면을 표시하십시오. 
* 클래식 인프라 탐색 메뉴에서 **네트워크 > DNS > DNS 되돌리기**를 선택하십시오.
* **IP 보기** 필드에 디바이스 목록에서 검색된 **공인 IP 주소**를 입력하십시오.
* **역방향 레코드** 세부사항을 포함하는 행의 어디든 클릭하여 편집을 위해 행을 여십시오.
* 아래 표를 기반으로 레코드에 대한 필드를 완료하거나 업데이트하십시오.<br/><br/><table border="1"><tbody><tr><th>필드</th><th>입력 항목</th></tr><tr><td>역방향 DNS</td><td>IP 주소가 해석할 호스트 이름</td></tr><tr><td>역방향 TTL</td><td>새 레코드에 대한 TTL(Time to Live)</td></tr><tr><td>참고</td><td>레코드에 관한 적용 가능한 모든 참고</td></tr></tbody></table><br/>
* 레코드를 업데이트하려면 **업데이트** 단추를 클릭하십시오. 조치를 취소하려면 **취소**를 클릭하십시오.

## 다음 작업
{:#add-or-edit-a-ptr-pointer-record-next}

PTR 레코드가 추가된 후, 해당 레코드와 연관된 공인 IP 주소가 레코드에서 지정된 호스트 이름으로 해석됩니다. 레코드는 언제든지 편집할 수 있습니다. PTR 레코드에서 세부사항을 제거하려면 **편집** 프로세스를 사용하여 필드에서 모든 정보를 삭제하십시오.
