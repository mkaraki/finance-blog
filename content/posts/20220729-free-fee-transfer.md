---
title: "銀行各社の送金無料相手"
date: 2022-07-29T00:00:00+09:00
draft: false
toc: false
---

振替などを利用した場合も含む各社の無料振込対応銀行のダイアグラムです。

## 前提条件

- すべての銀行を網羅しているわけではありません。
- 自動入金サービスによる取引は表内に入っていません。
- 最安の手数料です。インターネットバンキング限定などの制限などがあります。
- 本人口座間のお取引を前提としています。
  下記のご利用の際は本人口座以外への振込・振替が有料になります。
  - Jcoin Pay, Coin+の振替を利用する場合
  - SMBC-PayPay銀行間のお取引

## 実際の表

{{<mermaid align="center">}}

classDiagram
  class Coinプラス {
    決済サービス
    出金時3営業日
  }
  class Jcoin Pay {
    決済サービス
    翌営業日
  }

  auじぶん銀行<-->三菱UFJ銀行
  三菱UFJ銀行<-->三菱UFJ信託銀行

  SMBC信託銀行<-->三井住友銀行
  PayPay銀行<-->三井住友銀行 : SMBCポイントパック<br/>条件達成が必須

  住信SBIネット銀行<-->三井住友信託銀行

  三菱UFJ銀行<..>Coinプラス
  埼玉りそな銀行<..>Coinプラス
  三井住友銀行<..>Coinプラス
  Coinプラス<..>銀行CJ
  Coinプラス<..>Coinプラス対応銀行

  りそなグループ<..>Coinプラス

  class りそなグループ {
    りそな銀行
    埼玉りそな銀行
    関西みらい銀行
  }
  りそなグループ<-->みなと銀行

  class 銀行CJ {
    Jcoin PayとCoin+に対応
  }

  三井住友信託銀行<..>Jcoin Pay
  銀行CJ<..>Jcoin Pay

  みずほ信託銀行<--みずほ銀行

  Jcoin Pay<..>みずほ銀行
  Jcoin Pay<..>Jcoin Pay対応銀行


{{</mermaid >}}

- 描画ツールの都合で`Coin+`が`Coinプラス`と表記されている箇所があります。

## リンク

- [Jcoin Pay対応銀行](https://j-coin.jp/user/bank/)
- [COIN+対応銀行](https://faq.coinplus.jp/hc/ja/articles/4409252813721)