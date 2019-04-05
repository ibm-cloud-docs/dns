---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: DNS Zone, DNS management, Add DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS-Zone hinzufügen
{:#add-a-dns-zone}

Das DNS-Management mit {{site.data.keyword.BluSoftlayer_notm}} ist auch für DNS-Zonen verfügbar, die möglicherweise nicht zum {{site.data.keyword.BluSoftlayer_notm}}-Netz gehören. Über Ihre Schnittstelle können Sie jederzeit einzelne oder mehrere DNS-Zonen hinzufügen. Das Hinzufügen von DNS-Zonen erfolgt gegenwärtig in der Version [Control](https://control.softlayer.com/) des Kundenportals. Führen Sie die folgenden Schritte aus, um eine oder mehrere DNS-Zonen hinzuzufügen.

* Melden Sie sich bei der Version [Control](https://control.softlayer.com/) des Kundenportals mit Ihren eindeutigen Berechtigungsnachweisen an.
* Wählen Sie im Navigationsmenü die Option **Klassische Infrastruktur** aus.
* Wählen Sie **DNS** im Dropdown-Menü **Netz** aus.
* Wählen Sie **Forward-Zonen** aus.
* Wählen Sie die Registerkarte **DNS-Zone hinzufügen** in der rechten oberen Ecke aus.
* Legen Sie fest, ob eine einzelne Domäne oder mehrere Domänen hinzugefügt werden sollen:<br> <br><table border="1"><tbody><tr><th>Hinzufügen von...</th><th>Vorgehensweise</th></tr><tr><td>Einzelne Domäne</td><td>Führen Sie die folgenden Schritte im Abschnitt <strong>Einzelne Domäne hinzufügen</strong> der Anzeige aus:<br> <ul><li>Geben Sie den <strong>Namen der Domäne</strong> in das Feld <strong>Domänenname</strong> ein.</li><li>Geben Sie die <strong>IP-Adresse</strong>, auf die der Domänenname verweist, in das Feld <strong>IP-Adresse</strong> ein.</li><li>Klicken Sie auf die Schaltfläche <strong>Zone hinzufügen</strong>, um die Domäne hinzuzufügen.<br> </li></ul></td></tr><tr><td>Mehrere Domänen</td><td>Legen Sie fest, ob die Domänen einer oder mehreren IP-Adressen zugeordnet werden sollen:<br> <p> </p><p> </p><p> </p><p> </p><ul><li>Wenn die Domänen einer einzelnen IP-Adresse zugeordnet werden:<ul><li>Geben Sie <strong>die einzelnen Domänen</strong> in das Textfeld <strong>Domänen</strong> ein.</li><li>Geben Sie die <strong>IP-Adresse</strong> in das Feld <strong>Standard-IP-Adresse</strong> ein.</li><li>Klicken Sie auf die Schaltfläche <strong>Zone hinzufügen</strong>, um die angegebenen Domänen auf einmal hinzuzufügen.</li></ul></li><li>Wenn die Domänen mehreren IP-Adressen zugeordnet werden:<ul><li>Geben Sie jede <strong>einzelne Domäne</strong> mit der zugehörigen <strong>IP-Adresse</strong> in einer separaten Zeile in das Textfeld <strong>Domänen</strong> ein.</li><li>Klicken Sie auf die Schaltfläche <strong>Zone hinzufügen</strong>, um die angegebenen Domänen auf einmal hinzuzufügen.</li></ul></li><li> </li></ul></td></tr></tbody></table>

## Weitere Schritte
{:#add-a-dns-zone-next}

Die neu hinzugefügte DNS-Zone wird in der Liste der DNS-Zonen in der [Anzeige 'DNS-Zonen'](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens) im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/) angezeigt. Sie können die Zone jederzeit [bearbeiten](/docs/infrastructure/dns?topic=dns-edit-a-dns-zone-record) oder [löschen](/docs/infrastructure/dns?topic=dns-delete-a-dns-zone) werden.


