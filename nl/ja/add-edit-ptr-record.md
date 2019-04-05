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

# PTR (ポインター) レコードの追加または編集
{:#add-or-edit-a-ptr-pointer-record}

PTR (ポインター) レコードは、IP アドレスをホスト名に解決します。 ユーザーは、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/){:new_window} のリバース DNS 機能を使用して、IP アドレスに関連付けられる PTR レコードを追加することができます。 また、PTR レコードは、追加されたときと同じ方法で編集することもできます。 デバイスの PTR レコードを追加または編集するには、以下の手順に従ってください。

* PTR レコードを受け取るデバイスの**パブリック IP アドレス**を、**デバイス・リスト**から取得します。
* ナビゲーション・メニューから**「クラシック・インフラストラクチャー**」**を選択して、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「リバース DNS レコード」**画面を表示します。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「リバース DNS」**を選択します。
* デバイス・リストから取得した**パブリック IP アドレス**を、**「IP の表示 (View IP)」**フィールドに入力します。
* **リバース・レコード**の詳細が入っている行のいずれかの場所をクリックして、編集対象の行を開きます。
* 下の表に基づいて、レコードのフィールドを完成または更新します。<br/><br/><table border="1"><tbody><tr><th>フィールド</th><th>項目</th></tr><tr><td>リバース DNS</td><td>IP アドレスが解決されるホスト名</td></tr><tr><td>リバース TTL</td><td>新規レコードの存続時間 (TTL)</td></tr><tr><td>メモ</td><td>レコードに関する、該当するメモ</td></tr></tbody></table><br/>
* **「更新」**ボタンをクリックして、レコードを更新します。 アクションを取り消すには、**「キャンセル」**をクリックしてください。

## 次のステップ
{:#add-or-edit-a-ptr-pointer-record-next}

PTR レコードが追加された後、そのレコードに関連付けられているパブリック IP アドレスは、レコードに指定されたホスト名に解決されます。 レコードはいつでも編集できます。 PTR レコードから詳細を削除するには、**編集**プロセスで、すべての情報をフィールドから削除してください。
