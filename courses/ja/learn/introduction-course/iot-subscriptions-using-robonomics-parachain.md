---
title: "Lesson #5, IoT Subscriptions Using Robonomics Parachain"
lastUpdate: Thu May 04 2023 12:53:55 GMT+0400 (Samara Standard Time)
description: Robonomics Parachainを使用してIoTサブスクリプションを購入する方法を学びます。
lessonNumber: 5
metaOptions: [学ぶ, Robonomicsのアイデアについての紹介]
defaultName:  Introduction to the ideas of Robonomics
---

導入コースの最後のレッスンは、ある程度の忍耐が必要となるため、おそらく最も難しいレッスンです。 当社のネットワークの実際のトークンを使用して、ロボノミクス パラチェーンで IoT サブスクリプションを購入する方法を学びます。


## イントロ

IoTサブスクリプションは、サイバー物理システムのデジタルツインの状態を変更し、それに関する情報をPolkadot / Kusamaエコシステムを使用して保存するためのアクセスキーです。1つのサブスクリプションを所有すると、ユーザーはトランザクション手数料を支払う必要がなくなります。代わりに、ユーザーは一定期間に1回無料のトランザクションを送信できます。

サブスクリプションを購入する主な方法は、サブスクリプションオークションに参加することです。したがって、このレッスンでは、入札を行い、トランザクションを送信するためにXRTトークンを取得る必要があります。このプロセスに関する詳細情報は、[当社のwiki](https://wiki.robonomics.netwまたはk/docs/get-subscription)でも入手できます。

## 手順

<List type="numbers">

<li>

Robonomics ParachainトークンであるXRTトークンを約2つ必要とします（[トークンについて](https://robonomics.netwまたはk/xrt/)）。それらを持っていない場合、いくつかのオプションがあります。

a) レッスン2とレッスン4の両方のテストを90％の正解率で合格した場合、レッスンのために無料のトークンをリクエストできます。[特別なチェックdapp](https://lk.robonomics.academy/)でスコアを確認してください。具体的には、レッスン2では17問中15問、レッスン4では11問中10問を正解する必要があり、2回の試行があります。トークンを取得するには、[Discord](https://discord.gg/xqDgG3EGm9)（IBerman＃5862）のアカデミー管理者に連絡してください。

b) 1つの取引所でXRTトークンを購入します（[取引所のリスト](https://www.coingecko.com/en/coins/robonomics-network#markets/)を確認してください）。暗号通貨取引所に慣れていない場合は注意してください。暗号通貨取引所でのすべての購入には潜在的なリスクがある可能性があため、このレッスンを合格するために必要な量のトークンのみを購入してください。また、RobonomicsはEthereumとKusamaの2つのネットワークで存在していることを念頭に置いておいてください。したがって、各ネットワークには独自のXRTトークンがあります。Kusamaネットワークのパラチェーンで使用されるトークンが必要です。

c) Ethereumネットワーク（ERC-20形式）にXRTトークンを持っている場合は、[Exodus](https://old.dapp.robonomics.network/#/exodus)プロセスを使用してトークンをEthereumネットワークからKusamaネットワークに転送します。トークンの転送は週に1回行われることに注意してください。

</li>

<li>

IoTサブスクリプションは、最高入札者がサブスクリプションを取得するオークションプロセスを通じて購入されます。

オークションに参加する前に、利用可能なオークションがあるかどうかを確認する必要があります。Chain stateメニューを使用してRobonomics [Polkadot/Substrate portal](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fkusama.rpc.robonomics.network%2F#/chainstate)を開きます。 <code>rws</code>クエリを選択し、<code>auctionQueue()</code>を押します。＋ボタンを押すと、利用可能なオークションのIDが表示されます。表示されない場合や利用できない場合は、"[🎓robonomics-academy](https://discord.com/channels/803947358492557312/803947358492557315)"チャンネルで当社にお問い合わせください。

同じChain stateメニューで、<code>rws</code>を選択し、<code>auction(u32): Option&lt;PalletRobonomicsRwsAuctionLedger&gt;</code>を選択し、<code>u32</code>フィールドに覚えておいたオークションのIDを入力します。＋ボタンを押すと、興味深いオークションに関する情報が表示されます。 <code>winner</code>フィールドに<code>null</code>値がある場合、誰もこのサブスクリプションを持っていないため、取得を試みることができます。

</li>

<li>

XRTトークンで入札を行います。

開発者→外部メニューに移動し、前のレッスンで使用したPolkadot.jsアカウントと同じものを選択して、<code>rws</code>と<code>bid(index, amount)</code>のextrinsicを選択します。 <code>index</code>フィールドには、興味のあるオークションのIDを入力します。 <code>amount</code>フィールドには、入札用のトークン数を「ウィーナー」（1 XRT = 1,000,000,000 Wnに変換）して入力する必要があります。 当社の[dapp](https://dapp.robonomics.network/#/subscription)で現在の最低購読価格を確認してください。 

トランザクションを送信し、幸運ならIoTサブスクリプションを取得できます。 Polkadotアドレスが同じChain stateメニューを介してサブスクリプションを所有していることを確認できます。

</li>

<li>

最後のステップは、IoTサブスクリプション用のデバイスを追加することです。

これは単に、追加のPolkadotアドレスをサブスクリプションに割り当てることを意味します。これにより、それらがextrinsicsを実行できるようになります（たとえば、デバイスを起動したり、デバイスデータをブロックチーンに送信したりするため）。

まず、Robonomics Parachain用の新しいアカウントを作成します（[wiki](https://wiki.robonomics.network/docs/create-account-in-dapp/)のガイドに従います）、便宜上「スマートデバイス」と呼びます。

次に、開発者→外部メニューに移動し、<code>rws</code>と<code>setDevices()</code>を選択します。デバイスリストで「アイテムの追加」ボタンを使用してデバイスを追加し、最近作成したアカウントを選択します。その後、トランザクションを送信します。

デバイスアドレスはサブスクリプションに追加する必要があります。 Chain stateメニューで、サブスクリプションを持つPolkadot.jsアカウントに対して<code>rws</code>と<code>devices()</code>のクエリを使用して確認できます。

</li>

</List>

<Result>

IoTサブスクリプションを購入し、1つのデバイスを追加する成功したトランザクションを送信した後、レッスンは完了と見なされます。 トランザクションは、アカウントのPolkadotエクスプローラーに表示されるはずです。

[特別なチェックdapp](https://lk.robonomics.academy/)で結果を確認できます。コース中に使用されたPolkadot.jsの同じアカウントを使用して、チェックdappに認証してください。

</Result>