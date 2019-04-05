---
copyright:
  years: 1994, 2017, 2018, 2019
lastupdated: "2019-02-26"

keywords: Reverse DNS Record, Reverse DNS, IP address, Individual IP Select

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# リバース DNS レコードの更新
{:#update-reverse-dns-record}

ユーザーはリバース DNS を使用することで、IP アドレスに関連付けられているドメインを特定できます。 お客様はリバース DNS レコードをいつでも更新して PTR と存続時間 (TTL) を変更できます。 **バージョンの管理** ([IBM Cloud コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/)) 内で、**検索および置換**ツールを使用して PTR レコードを一括で更新できます。このツールを使用すれば、「検索」フィールドに PTR の一部または全部を入力して、該当する PTR 内の各オカレンスを希望の情報で置き換えることができます。 

このツールは、既存の PTR がサーバーまたは VLAN に関連付けられている場合にのみ機能することにご注意ください。 PTR が存在しない場合、詳細はリストされず、更新しようとするとエラーになります。 

リバース DNS レコードを追加するには、[『PTR (ポインター) レコードの追加と編集』](/docs/infrastructure/dns?topic=dns-add-or-edit-a-ptr-pointer-record)を参照してください。 リバース DNS レコードを更新するには、次の手順に従います。

 * 自分の固有の資格情報を使用して、[IBM Cloud コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/)にナビゲートします。
 * ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択します。
 * 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「リバース DNS」**を選択します。
 * IP アドレスを入力するか、ドロップダウン・メニューからそれを選択して、**「IP の表示」**をクリックします。
 * リストされたオプションを編集した後、**「保存」**をクリックします。**「このサブネットのすべての IP の RDNS を編集」**を選択して、サブネット全体にわたって変更を行うこともできます。 
 

