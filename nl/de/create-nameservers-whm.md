---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: create your own nameservers, cPanel, WHM

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# Eigene Namensserver in cPanel/WHM erstellen
{:#create-your-own-nameservers-in-cpanel-whm}

In diesem Artikel werden die Schritte zum Erstellen eigener Namensserver mit Web Host Manager (WHM) beschrieben. Falls nach der Ausführung dieser Schritte Probleme auftreten, erstellen Sie ein Support-Ticket das auf diesen Artikel verweist.

1. Legen Sie zuerst fest, wie Ihre Namensserver heißen sollen. Angenommen, das Hosting-Unternehmen trägt den Namen “Geniales Server-Hosting” und Sie möchten die Namensserver `ns1.genialesserverhosting.com` und `ns2.genialesserverhosting.com` einrichten.

* Melden Sie sich auf Ihrem Server bei WHM an, indem Sie In Ihrem Browser die Web-Adresse `https://XX.XX.XX.XX:2087` aufrufen.

* Wählen Sie zum Einrichten Ihrer Namensserver die erste Option (normalerweise “cPanel/WHM - Basiskonfiguration”) in der linken Seitenleiste aus. 

 * Mit dieser Option können Sie die Namen für Ihre primären, sekundären, tertiären und quartären Namensserver festlegen.

 * Wählen Sie anschließend die Schaltfläche “Speichern” aus.

2. Erstellen Sie nun die Zonendatei für `genialesserverhosting.com` auf Ihrem Server. Für diesen Vorgang stehen zwei verschiedene Methoden zur Verfügung:

Erste Methode: Erstellen Sie das Domänenkonto für “genialesserverhosting.com”. Die Anweisungen für diese Methode sind nicht Teil dieses Artikels. Weitere Informationen enthält die [cPanel-Dokumentation](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html): 

   * Wählen Sie in der linken Seitenleiste “DNS-Zone hinzufügen” unter “DNS-Funktionen” aus.

   * Geben Sie die IP-Adresse, unter der die Hauptwebsite für `genialesserverhosting.com` gehostet wird, und den Domänennamen an.

   **Hinweis: Führen Sie diesen Schritt nur aus, wenn `genialesserverhosting.com` nicht auf dem aktuellen Server gehostet werden soll!**

   * Klicken Sie unter der Überschrift **Netzbetrieb konfigurieren** auf **Namensserver-IPs**.

   * Geben Sie die Namen Ihrer Namensserver an. Geben Sie beispielsweise `ns1.genialesserverhosting.com` und danach
`ns2.genialesserverhosting.com` an.

   * Lokalisieren Sie in der linken Seitenleiste den Eintrag **Namensserver konfigurieren** unter **Servicekonfiguration**.

   * Eine Nachricht ähnlich der folgenden wird angezeigt: “We recommend you do not enable the nameserver unless you are going to use it. If you wish to disable the nameserver you can always turn it off in the Service Manager”.

   * Da Sie den Namensserver betriebsbereit machen möchten, wählen Sie die Schaltfläche **Weiter >>** aus. Das Tool `cPanel` prüft, dass die richtigen Pakete auf Ihrem Server installiert und für das Hosting Ihrer Domänennamensservices ordnungsgemäß konfiguriert sind. Damit ist dieser Vorgang abgeschlossen.

Externe Links

* [cPanel-Dokumentation](http://www.cpanel.net/support/docs/11//whm/account_functions_creatnewacct.html)
