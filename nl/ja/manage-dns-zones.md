---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-14"

keywords: DNS Zone, DNS management, Add DNS Zone, Edit DNS Zone, Delete DNS Zone

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:important: .important}
{:tip: .tip}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}

# DNS ゾーンの管理
{: #manage-dns-zones}

## DNS ゾーンの追加
{: #add-a-dns-zone}

{{site.data.keyword.cloud}} による DNS 管理は、{{site.data.keyword.cloud_notm}} ネットワーク上にない DNS ゾーンに対しても有効です。 用意されているインターフェースを使用することによって、いつでも DNS ゾーンを 1 つのドメインとして、または一括で追加できます。 DNS ゾーンの追加は現在、[IBM Cloud コンソール](https://{DomainName}/)で行われます。1 つ以上の DNS ゾーンを以下の手順で追加します。

* ユーザー固有の資格情報を使用して、[IBM Cloud コンソール](https://{DomainName}/)にログインします。
* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択します
* **「ネットワーク」**ドロップダウン・メニューから**「DNS」**を選択します。
* **「前方ゾーン (Forward Zones)」**を選択します。
* 右上にある**「DNS ゾーンの追加 (Add DNS Zone)」**タブを選択します。
* 1 つのドメインを追加するか、または複数のドメインを追加するかを決定します。

|追加する対象|手順|
|---|---|
|1 つのドメイン| 画面の**「単一ドメインの追加 (Add single domain)」**セクションで、次の手順を実行します。 <ul><li>**ドメイン・ネーム**を**「ドメイン・ネーム」**フィールドに入力します。</li><li>**「IP アドレス (IP Address)」**フィールドに、そのドメイン・ネームが指す **IP アドレス**を入力します。</li><li>**「ゾーンの追加 (Add Zone)」**ボタンをクリックして、ドメインを追加します。</li></ul>|
|複数のドメイン| ドメインが 1 つの IP アドレスに関連付けられるか、または複数の IP に関連付けられるかを決定します。 <ul><li>ドメインが 1 つの IP アドレスに関連付けられる場合: <ul><li>**「ドメイン」**テキスト・ボックスに、**それぞれのドメイン**を入力します。</li><li>**「デフォルト IP アドレス (Default IP Address)」**フィールドに、**IP アドレス**を入力します。</li><li>**「ゾーンの追加 (Add Zone)」**ボタンをクリックして、ドメインを一括で追加します。</li></ul></li><li>ドメインが複数の IP アドレスに関連付けられる場合: <ul><li>**「ドメイン」**テキスト・ボックスに、**それぞれのドメイン**および対応する **IP アドレス**を 1 行の項目として入力します。</li><li>**「ゾーンの追加 (Add Zone)」**ボタンをクリックして、ドメインを一括で追加します。</li></ul></li></ul>


### 次のステップ
{:#add-a-dns-zone-next}

1 つのゾーンが正常に追加されると、「ゾーン編集 (Zone Edit)」ページに自動的にリダイレクトされます。
[IBM Cloud コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の [DNS ゾーン画面](/docs/infrastructure/dns?topic=dns-use-the-dns-zones-screens)にある DNS ゾーンのリストに、新しい DNS ゾーンが表示されます。ゾーンはいつでも[編集](#edit-a-dns-zone)または[削除](#delete-a-dns-zone)できます。

## DNS ゾーンの編集
{: edit-a-dns-zone}
DNS ゾーン画面のゾーンのリストから、編集する DNS ゾーンの名前をクリックして選択します。選択すると、「DNS ゾーンの編集 (DNS Edit Zone)」ページが開きます。このページで DNS ゾーンに変更を加え、**「SOA の更新 (Update SOA)」**をクリックして変更をコミットできます。 

**「DNS ゾーンの編集 (Edit a DNS Zone)」**画面を使用すると、編集中のゾーンの既存のレコードを編集したり、新しいレコードを追加したりできます。また、この画面からゾーンのエクスポートや削除もできます。

### 次のステップ
{:#edit-a-dns-zone-next}

**「すべての DNS ゾーンの表示 (View ALl DNS Zones)」**をクリックすると、DNS ゾーンのリストに戻ります。


## DNS ゾーンの削除
{: #delete-a-dns-zone}

DNS ゾーンを追加した後、そのゾーンをいつでも削除できます。 DNS ゾーンの削除は永久で、元に戻すことはできません。 DNS ゾーンを削除するには、以下の手順に従ってください。

* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択して、目的の**「DNS ゾーン (DNS Zone)」**画面にナビゲートします。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」**を選択し、必要なゾーンのタイプを選択します。
* 目的の DNS ゾーンが入っている行の末尾にある**「削除」**アイコンを選択してください。 ポップアップ確認ボックスが表示されます。
* 削除するには**「はい (Yes)」**ボタンを、アクションを取り消すには**「いいえ (No)」**ボタンを選択します。

また、「DNS ゾーンの編集 (Edit DNS Zones)」画面からゾーンを削除することもできます。
{:tip}

### 次のステップ
{:#delete-a-dns-zone-next}

DNS ゾーンを削除した後、そのゾーンを [IBM Cloud コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン ")](https://{DomainName}/) で管理することはできなくなります。削除したゾーンを再び「ダッシュボード」で管理するには、それを[新規ゾーンとして追加](#add-a-dns-zone)する必要があります。
