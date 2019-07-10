---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-05-31"

keywords: Secondary DNS Zone, IBM Cloud, Add Secondary Zone, Edit Secondary Zone, Delete Secondary Zone, primary DNS Zones

subcollection: dns

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:DomainName: data-hd-keyref="DomainName"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:deprecated: .deprecated}
{:generic: data-hd-programlang="generic"}


# 2 次 DNS ゾーンの管理
{: #manage-secondary-dns-zones}

データ損失の対策として 1 次 DNS ゾーンをキャッシングする手段として、{{site.data.keyword.cloud}} は 2 次 DNS をすべてのお客様に提供しています。 2 次 DNS ゾーンの保守は必須ではありませんが、複数のドメインを持つユーザーには強くお勧めします。 


## 2 次 DNS ゾーンの追加
{:#add-a-secondary-dns-zone}

2 次 DNS ゾーンを追加するには、以下の手順に従ってください。

* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択して、[{{site.data.keyword.cloud_notm}} コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面に移動します。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「セカンダリー・ゾーン」**を選択します。
* **「ゾーンの追加 (Add Zone)」**タブを選択します。
* **「ゾーン (Zone)」**フィールドに**ゾーンのドメイン**を入力します。
* **「マスター・ネーム・サーバー (Master Nameserver)」**フィールドに**マスター・ネーム・サーバーの IP アドレス**を入力します。
* **「転送間隔 (Transfer Interval)」**フィールドに、1 次 DNS ゾーンが 2 次 DNS ゾーンに転送されるときの**転送時間** (分) を入力します。
* そのゾーンを追加するには**「追加 (Add)」**ボタンを、アクションを取り消すには**「キャンセル」**を選択します。

### 追加後の状態
{:#add-a-secondary-dns-zone-next}

2 次 DNS ゾーンを作成した後、そのゾーンは「2 次 DNS ゾーン (Secondary DNS Zones)」画面のゾーンのリストに表示されます。 1 次ゾーンから 2 次ゾーンへのデータ転送は、ゾーンの作成時に指定した間隔で行われます。 そのゾーンはいつでも[編集](#edit-a-secondary-dns-zone)、[手動転送](/docs/infrastructure/dns?topic=dns-make-a-manual-zone-transfer-for-a-secondary-dns-zone)、または 1 次ゾーンに[変換](/docs/infrastructure/dns?topic=dns-convert-a-secondary-dns-zone-to-a-primary-zone)できます。 また、2 次 DNS ゾーンはいつでも[削除](#delete-a-secondary-dns-zone)できます。

## 2 次 DNS ゾーンの編集
{:#edit-a-secondary-dns-zone}

2 次 DNS ゾーンは、マスター・ネーム・サーバーや転送間隔を更新するためにいつでも編集できます。 2 次 DNS ゾーンを編集するには、以下の手順に従います。

* ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択して、[{{site.data.keyword.cloud_notm}} コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面に移動します。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「セカンダリー・ゾーン」**を選択します。
* ゾーンを編集のために開くには、**2 次 DNS ゾーンを含む行**で任意の場所をクリックします。
  複数の 2 次ゾーンが存在する場合、表示をフィルタリングして、編集が必要なゾーンを見つけることができます。
  {:note}  
* 必要に応じて**「マスター・ネーム・サーバー (Master Nameserver)」**フィールドと**「転送間隔 (Transfer Interval)」**フィールドを更新します。
* **「更新」**ボタンを選択して 2 次 DNS ゾーンを更新するか、または**「キャンセル」**を選択してアクションを取り消します。

### 編集後の状態
{:#edit-a-secondary-dns-zone-next}

2 次 DNS ゾーンの編集後、**「マスター・ネーム・サーバー (Master Nameserver)」**と**「転送間隔 (Transfer Interval)」**の値は更新を反映し、2 次ゾーンは新しい情報に基づいて転送を受信し始めます。 上記の手順を繰り返すことで、ゾーンをいつでも編集できます。

## 2 次 DNS ゾーンの削除
{:#delete-a-secondary-dns-zone}

2 次 DNS ゾーンを作成した後、そのゾーンをいつでも削除できます。 2 次 DNS ゾーンを削除すると、そのゾーンは検索できなくなることに注意してください。 2 次 DNS レコードを削除するには、以下の手順に従います。

 * ナビゲーション・メニューから**「クラシック・インフラストラクチャー」**を選択して、[{{site.data.keyword.cloud_notm}} コンソール ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/) の**「2 次 DNS ゾーン (Secondary DNS Zones)」**画面に移動します。 
* 「クラシック・インフラストラクチャー」ナビゲーション・メニューから**「ネットワーク」>「DNS」>「セカンダリー・ゾーン」**を選択します。
* 削除が必要なゾーンの**「アクション」**ドロップダウン・リストで**「削除」**を選択します。 ポップアップ確認ボックスが表示されます。
  複数の 2 次ゾーンが存在する場合、表示をフィルタリングして、削除対象のゾーンを見つけることができます。
  {:note}
* 削除するには**「はい (Yes)」**ボタンを、アクションを取り消すには**「いいえ (No)」**ボタンを選択します。

### 削除後の状態
{:#delete-a-secondary-dns-zone-next}

2 次 DNS ゾーンが削除されると、1 次ゾーンからの自動転送は停止し、2 次ゾーンは存在しなくなります。 どの時点であっても、2 次 DNS ゾーンが 1 次ゾーンに必要になった場合は、新しい[2 次 DNS ゾーンを作成](#add-a-secondary-dns-zone)することができます。
