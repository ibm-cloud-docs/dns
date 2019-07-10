---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-15"

keywords: Transfer Existing Domain, Transfer multiple domains 

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ドメインの転送
{: #transfer-domains}

## 既存ドメインの IBM Cloud への転送
{:#transfer-an-existing-domain-to-ibm-cloud}

登録されたドメインをいつでも転送できます。サード・パーティーのレジストラーから {{site.data.keyword.cloud}} にドメインを転送すれば、ドメイン管理プロセスを簡素化できます。 ドメインを転送しても、Web サイト、E メール、DNS に影響はありません。 ドメイン・レコードを管理するレジストラーが変更されるだけです。 既存のドメインを {{site.data.keyword.cloud_notm}} に転送するには、この記事にある手順に従います。

## 1 つのドメインの転送
{: #transfer-single-domain}

* [{{site.data.keyword.cloud_notm}} コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「ドメイン登録 (Domain Registration)」**画面に移動します。[『「ドメイン登録 (Domain Registration)」画面へのアクセス』](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen)を参照してください。
* **「転送 (Transfer)」**タブを選択します。
* **「ドメイン・ネーム (Domain Name)」**フィールドに既存のドメイン・ネームを入力します。
* **「ドメイン・タイプ (Domain Type)」**ドロップダウン・リストからドメイン・タイプを選択します。
* ドメインがアクティブでい続ける時間を**「登録時間 (Registration Time)」**ドロップダウン・リストから選択します。

  期間ごとの価格が時間の横に表示され、ドメインの更新時にクレジット・カードに請求されるか、またはアカウント (口座) のクレジット (預金) から差し引かれることになります。
  {:note}
  
* **「続行」**ボタンを選択してドメインを転送します。

## 複数ドメインの転送
{: #transfer-multiple-domains}

有効なクレジット・カードがある場合や、使用可能なクレジットがアカウントにある場合は、いつでも複数のドメインを個別にではなく一括して {{site.data.keyword.cloud_notm}} に転送できます。 {{site.data.keyword.cloud_notm}} の複数ドメインを転送するには、次の手順に従います。

* [{{site.data.keyword.cloud_notm}} コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「ドメイン登録 (Domain Registration)」**画面に移動します。[『「ドメイン登録 (Domain Registration)」画面へのアクセス』](/docs/infrastructure/dns?topic=dns-how-to-use-the-domain-registration-screen)を参照してください。
* **「転送 (Transfer)」**タブを選択します。
* **「転送 (Transfer)」**タブ内で**「複数ドメインの転送 (Transfer Multiple Domains?)」**オプションを選択します。
* **「ドメイン・ネーム (Domain Name)」**フィールドに既存のドメイン・ネームを入力します。
* **「ドメイン・タイプ (Domain Type)」**ドロップダウン・リストからドメイン・タイプを選択します。
* 転送されたドメインがアクティブでい続ける時間を**「登録時間 (Registration Time)」**ドロップダウン・リストから選択します。

期間ごとの価格が時間の横に表示され、ドメインの更新時にクレジット・カードに請求されるか、またはアカウント (口座) のクレジット (預金) から差し引かれることになります。
{:note}

* 転送する追加のドメインごとに繰り返します。

さらにドメイン・エントリーを増やすために追加のブランク・フィールドを取り込むには、**「さらに追加」**オプションを選択します。 画面から 1 つのエントリー全体を削除するには、**「削除」**アイコンを選択します。
{:note}

* **「続行」**ボタンを選択してドメインを転送します。



## 次のステップ
{:#transfer-an-existing-domain-to-ibm-cloud-next}

転送したドメインは、[カスタマー・ポータル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/) 内で管理できます。 ドメインの登録有効期限が近づいているときは、**「ドメイン管理 (Domain Management)」**画面でドメインを[更新](/docs/infrastructure/dns?topic=dns-renew-an-existing-domain)できます。
