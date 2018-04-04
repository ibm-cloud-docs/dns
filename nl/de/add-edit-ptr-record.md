---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-11"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Zeigerdatensatz (PTR) hinzufügen oder bearbeiten

Zeigerdatensätze (Pointer, PTR) lösen IP-Adressen in Hostnamen auf. Benutzer können PTR-Datensätze, die einer IP-Adresse zugeordnet werden sollen, über die Funktion 'Reverse DNS' im [Kundenportal ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){:new_window} hinzufügen. Darüber hinaus können PTR-Datensätze mit der gleichen Methode bearbeitet werden, mit der sie hinzugefügt wurden. Führen Sie die folgenden Schritte aus, um einen PTR-Datensatz für eine Einheit hinzuzufügen oder zu bearbeiten:

1. Rufen Sie die **Öffentliche IP-Adresse** für die Einheit, die den PTR-Datensatz empfangen soll, aus der **Einheitenliste** ab.
* Öffnen Sie die Anzeige **Reverse DNS-Datensätze**. Weitere Informationen finden Sie unter [Anzeige 'DNS-Zonen' verwenden](use-dns-zones-screen.html).
* Geben Sie die **öffentliche IP-Adresse**, die Sie aus der Einheitenliste abgerufen haben, in das Feld **IP-Adresse zum Anzeigen** ein.
* Klicken Sie auf ein beliebige Stelle in der Zeile mit den Details des **Reverse-Datensatzes**, um die Zeile zum Bearbeiten zu öffnen.
* Füllen oder aktualisieren Sie die Felder für den Datensatz gemäß der nachfolgenden Tabelle:<br/><br/><table border="1"><tbody><tr><th>Feld</th><th>Eintrag</th></tr><tr><td>Reverse DNS</td><td>Der Hostname, in den die IP-Adresse aufgelöst wird.</td></tr><tr><td>Reverse-TTL</td><td>Die Lebensdauer (Time to Live, TTL) für den neuen Datensatz.</td></tr><tr><td>Hinweise</td><td>Alle zugehörigen Hinweise zu dem Datensatz</td></tr></tbody></table><br/>
* Klicken Sie auf die Schaltfläche **Aktualisieren**, um den Datensatz zu aktualisieren. Klicken Sie auf **Abbrechen**, um die Aktion abzubrechen.

## Weitere Schritte

Nachdem ein PTR-Datensatz hinzugefügt wurde, wird die dem Datensatz zugeordnete öffentliche IP-Adresse in den Hostnamen aufgelöst, der im Datensatz angegeben ist. Der Datensatz kann jederzeit bearbeitet werden. Um Details aus dem PTR-Datensatz zu entfernen, löschen Sie die betreffenden Informationen mit der Aktion **Bearbeiten** vollständig aus den Feldern.
