---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-08"

keywords: Delete Custom Name Servers, Lock Domain Select, Domain Domains

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# ドメインのカスタム・ネーム・サーバーの追加、編集、または削除
{:#add-edit-or-delete-custom-name-servers-for-a-domain}

{{site.data.keyword.BluSoftlayer_notm}} ネットワーク上で稼働するドメインは、最大 5 つのカスタム・ネーム・サーバーを指すことができます。 カスタム・ネーム・サーバーは、いつでもユーザーによって追加、削除、または変更できます。 ドメインのカスタム・ネーム・サーバーを追加、編集、または削除するには、以下の手順に従ってください。

1. ブラウザーで[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/){: new_window} を開いて、ご使用のアカウントにログインします。
2. カスタマー・ポータル・ナビゲーションで、ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択します。
1. 「クラシック・インフラストラクチャー」ナビゲーション・メニューから、**「サービス」>「ドメイン登録」**を選択します。
3. 目的の**ドメイン・ネーム**を選択して、ドメインをそのスナップショット・ビューに展開します。
4. **「ドメインのロック (Lock Domain)」**で**「アンロック (Unlocked)」**を選択します。
5. 画面の**「カスタム・ネーム・サーバー (Custom Name Servers)」**セクションで**「NS の追加/編集 (Add/Edit NS)」**を選択してください。 ポップアップ ボックスが表示されます。
6. 下の表を参照して、目的の作業に基づいたアクションを実行します。<br/><br/><table border="1"><tbody><tr><th>作業</th><th>アクション</th></tr><tr><td>カスタム・ネーム・サーバーの追加</td><td>ネーム・サーバーのホスト名を空のフィールドに入力します。</td></tr><tr><td>カスタム・ネーム・サーバーの削除</td><td>該当するネーム・サーバーのフィールドから情報を削除します。</td></tr><tr><td>カスタム・ネーム・サーバーの編集</td><td>該当するネーム・サーバーの適切なフィールドで詳細を編集します。</td></tr></tbody></table>
7. 変更内容を保存するには**「関連付け (Associate)」**ボタンを、アクションを取り消すには**「キャンセル」**を選択します。

## 次のステップ
{:#add-edit-or-delete-custom-name-servers-for-a-domain-next}

ネーム・サーバーの詳細を更新した後、それらはドメインの**「カスタム・ネーム・サーバー (Custom Name Servers)」**セクションの下に表示されます。 詳細はいつでも更新できます。
