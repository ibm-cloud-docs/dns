---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Manual Zone Transfer, DNS Zone transfers, Secondary DNS Zone

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# 보조 DNS 구역에 대한 수동 구역 전송 작성
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

일반적으로 DNS 구역 전송은 사용자가 지정한 보조 DNS 전송 간격을 바탕으로 자동으로 완료됩니다. 수동 구역 전송을 사용하여 그렇지 않으면 다음 자동 전송까지 대기하는 전송할 컨텐츠를 강제 실행할 수 있습니다. 수동 전송을 완료하려면 [보조 DNS 구역이 설정되어야 합니다](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone). 보조 DNS에 대한 수동 구역 전송을 작성하려면 이 문서의 단계를 따르십시오.

1. [고객 포털 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/)의 **보조 DNS 구역** 화면으로 이동하십시오. [DNS 구역 화면 사용](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window}을 참조하십시오.
2. **조치** 드롭 다운 목록에서 **전송 강제 실행**을 선택하여 전송을 시작하십시오.

## 다음 작업
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone-next}

전송이 시작된 후, 상태가 **지금 전송 중**으로 변경됩니다. 수동 전송은 시작된 후에는 취소할 수 없습니다. 데이터가 전송된 후, 데이터 전송은 보조 DNS에 대해 이전에 설정된 전송 간격으로 돌아갑니다. 빈번하게 수동 구역 전송을 작성할 필요성을 피하기 위해 언제든지 [전송 간격을 변경할 수 있습니다](/docs/infrastructure/dns?topic=dns-edit-a-secondary-dns-zone).
