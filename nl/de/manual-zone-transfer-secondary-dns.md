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


# Manuelle Zonenübertragung für sekundäre DNS-Zone durchführen
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone}

Im Allgemeinen werden DNS-Zonenübertragungen in dem von Ihnen angegebenen Übertragungsintervall für sekundäres DNS automatisch durchgeführt. Sie können eine manuelle Zonenübertragung verwenden, um die Übertragung von Inhalten zu erzwingen, die andernfalls bis zur nächsten automatischen Übertragung warten müssen. Zum Durchführen einer manuellen Übertragung müssen Sie eine [sekundäre DNS-Zone einrichten](/docs/infrastructure/dns?topic=dns-add-a-secondary-dns-zone). Führen Sie die im vorliegenden Abschnitt beschriebenen Schritte aus, um eine manuelle Zonenübertragung für ein sekundäres DNS durchzuführen.

1. Navigieren Sie zur Anzeige **Sekundäre DNS-Zonen** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/). Weitere Informationen finden Sie unter [Anzeige 'DNS-Zonen' verwenden](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen){:new_window}.
2. Wählen Sie **Übertragung erzwingen** in der Dropdown-Liste **Aktionen** aus, um die Übertragung zu starten.

## Weitere Schritte
{:#make-a-manual-zone-transfer-for-a-secondary-dns-zone-next}

Wenn die Übertragung beginnt, wird der Status in **Übertragung läuft** geändert. Manuelle Übertragungen können nicht abgebrochen werden, nachdem Sie gestartet wurden. Nachdem die Datenübertragung abgeschlossen ist, wird wieder das Übertragungsintervall verwendet, das für das sekundäre DNS festgelegt wurde. Sie können das [Übertragungsintervall jederzeit ändern](/docs/infrastructure/dns?topic=dns-edit-a-secondary-dns-zone), um häufige manuelle Zonenübertragungen zu vermeiden.
