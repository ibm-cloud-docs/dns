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

# Zeigerdatensatz (PTR) hinzufügen oder bearbeiten
{:#add-or-edit-a-ptr-pointer-record}

Zeigerdatensätze (Pointer, PTR) lösen IP-Adressen in Hostnamen auf. Benutzer können PTR-Datensätze, die einer IP-Adresse zugeordnet werden sollen, über die Funktion 'Reverse DNS' im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/){:new_window} hinzufügen. Darüber hinaus können PTR-Datensätze mit der gleichen Methode bearbeitet werden, mit der sie hinzugefügt wurden. Führen Sie die folgenden Schritte aus, um einen PTR-Datensatz für eine Einheit hinzuzufügen oder zu bearbeiten:

* Rufen Sie die **Öffentliche IP-Adresse** für die Einheit, die den PTR-Datensatz empfangen soll, aus der **Einheitenliste** ab.
* Rufen Sie die Anzeige **Reverse DNS-Datensätze** ** im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/) auf, indem Sie im Navigationsmenü die Option **Klassische Infrastruktur** auswählen. 
* Wählen Sie im Navigationsmenü 'Klassische Infrastruktur' die Optionen **Netz > DNS > Reverse DNS** aus.
* Geben Sie die **öffentliche IP-Adresse**, die Sie aus der Einheitenliste abgerufen haben, in das Feld **IP-Adresse zum Anzeigen** ein.
* Klicken Sie auf ein beliebige Stelle in der Zeile mit den Details des **Reverse-Datensatzes**, um die Zeile zum Bearbeiten zu öffnen.
* Füllen oder aktualisieren Sie die Felder für den Datensatz gemäß der nachfolgenden Tabelle:<br/><br/><table border="1"><tbody><tr><th>Feld</th><th>Eintrag</th></tr><tr><td>Reverse DNS</td><td>Der Hostname, in den die IP-Adresse aufgelöst wird.</td></tr><tr><td>Reverse-TTL</td><td>Die Lebensdauer (Time to Live, TTL) für den neuen Datensatz.</td></tr><tr><td>Hinweise</td><td>Alle zugehörigen Hinweise zu dem Datensatz</td></tr></tbody></table><br/>
* Klicken Sie auf die Schaltfläche **Aktualisieren**, um den Datensatz zu aktualisieren. Klicken Sie auf **Abbrechen**, um die Aktion abzubrechen.

## Weitere Schritte
{:#add-or-edit-a-ptr-pointer-record-next}

Nachdem ein PTR-Datensatz hinzugefügt wurde, wird die dem Datensatz zugeordnete öffentliche IP-Adresse in den Hostnamen aufgelöst, der im Datensatz angegeben ist. Der Datensatz kann jederzeit bearbeitet werden. Um Details aus dem PTR-Datensatz zu entfernen, löschen Sie die betreffenden Informationen mit der Aktion **Bearbeiten** vollständig aus den Feldern.
