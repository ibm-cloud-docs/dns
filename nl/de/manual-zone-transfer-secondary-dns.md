---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Manuelle Zonenübertragung für sekundäre DNS-Zone durchführen

Im Allgemeinen werden DNS-Zonenübertragungen in dem von Ihnen angegebenen Übertragungsintervall für sekundäres DNS automatisch durchgeführt. Sie können eine manuelle Zonenübertragung verwenden, um die Übertragung von Inhalten zu erzwingen, die andernfalls bis zur nächsten automatischen Übertragung warten müssen. Zum Durchführen einer manuellen Übertragung müssen Sie eine [sekundäre DNS-Zone einrichten](add-secondary-dns-zone.html). Führen Sie die im vorliegenden Abschnitt beschriebenen Schritte aus, um eine manuelle Zonenübertragung für ein sekundäres DNS durchzuführen.

1. Navigieren Sie zur Anzeige **Sekundäre DNS-Zonen** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/). Weitere Informationen finden Sie unter [Anzeige 'DNS-Zonen' verwenden](delete-secondary-dns-record.html){:new_window}.
2. Wählen Sie **Übertragung erzwingen** in der Dropdown-Liste **Aktionen** aus, um die Übertragung zu starten.

## Weitere Schritte

Wenn die Übertragung beginnt, wird der Status in **Übertragung läuft** geändert. Manuelle Übertragungen können nicht abgebrochen werden, nachdem Sie gestartet wurden. Nachdem die Datenübertragung abgeschlossen ist, wird wieder das Übertragungsintervall verwendet, das für das sekundäre DNS festgelegt wurde. Sie können das [Übertragungsintervall jederzeit ändern](edit-secondary-dns-zone.html), um häufige manuelle Zonenübertragungen zu vermeiden.
