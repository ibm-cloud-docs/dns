---

copyright:
  years: 1994, 2017-2019
lastupdated: "2019-03-07"

keywords: Secondary Domain FAQ, zone transfers, IBM Cloud DNS servers

subcollection: dns

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 2 次ドメイン FAQ
{:#secondary-domain-faq}

## 自分の 2 次ドメインに対して応答する IBM Cloud DNS サーバーは?
{:#what-ibm-cloud-dns-servers-will-answer-for-my-secondary-domains}

IBM Cloud のエニーキャスト IPv6 対応権限 DNS サーバー:

 * ns1.softlayer.com
 * ns2.softlayer.com

## ゾーン転送の起点は?
{:#where-will-the-zone-transfers-come-from}

ご使用の 2 次ドメインの転送は、4 つある IP アドレスのいずれかから行われます。

  * 66.228.118.67
  * 67.228.119.235
  * 208.43.119.235
  * 12.96.161.249

## ドメイン転送後に、そのドメイン、またはそのドメインに対する変更が表示されるまでにかかる時間は?
{:#how-long-does-it-take-for-changes-to-become-visible}

ドメイン、およびそのドメインに対する変更は転送完了直後に IBM Cloud DNS サーバーに表示されます。 DNS のキャッシングおよび伝搬の性質上、変更が他の DNS サーバーで表示されるまでには、しばらく時間がかかる場合があります。  

## ゾーン更新通知はサポートされていますか?
{:#are-zone-update-notifies-supported}

現時点では通知はサポートされていません。

## 「即時転送 (Transfer Now)」ボタンを押した場合にかかる時間は?
{:#how-immediate-is-the-transfer-now-button}

「即時転送 (Transfer Now)」ボタンをクリックしてからドメインが転送されるまでに 1 分くらいかかります。

## プライベート・ネットワーク上でマスターを構成できますか? それとも、パブリック・ネットワークを経由させる必要がありますか?
{:#can-a-master-be-configured-on-private-network}

現時点では、できません。 AXFR 要求はすべてパブリック・ネットワーク経由で行われます。

## マスターが使用不可になってから数日でスレーブは削除されますか?
{:#are-slaves-removed-after-days-master-is-unavailable}

長期にわたってドメインのマスターがダウンしていたり構成が間違っていたりする場合、当社はドメインの転送試行を止めます。  ゾーンの転送に問題があり、その結果としてゾーンが使用不可となった場合は、ポータルからお客様にフィードバックが提供され (「エラー・メッセージ (Error Messages)」タブ)、ドメインを再びアクティブにする方法が示されます (「手動ゾーン転送 (Manual Zone Transfer)」タブ)。

## 転送の間隔は 1 分以上空ける必要がありますか?
{:#is-1minute-lowest-transfer-frequency}

はい。

## 転送間隔を 1920 分に設定してから 10 分に再設定した場合は、最初に 1920 分経過するまで待ってからでないと新しい間隔 (10 分) は反映されないのでしょうか?
{:#frequency-change-expiration-effects}

いいえ。システムにおいて再転送キューが計算され、前回の転送試行時刻に新規設定の間隔 (10 分) が追加されます。  そのため、転送間隔を 1920 分に設定してから 10 分に変更した場合に、前回の転送試行から 10 分以上経過しているのであれば、当社は転送を即時に再試行し、その後は 10 分間隔で転送を再試行します。
