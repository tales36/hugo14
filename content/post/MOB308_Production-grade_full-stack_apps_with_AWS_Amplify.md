---
title: "MOB308_Production Grade_full Stack_apps_with_AWS_Amplify"
date: 2019-12-03T02:26:12+09:00
author: "katsutoshi miyata"
tags: ["勉強系","AWS re:invent2019"]
cover: ../../img/awsreinvent2019.jpg
---

## 飛行機の予約システムつくってみた

### ■フロントエンドがAmplifyで動くアプリ

飛行機の離陸、着陸時間が調べられるページ、プロフィールページ、  
飛行機の予約ができる/情報が見れるページの3ページ分。

プロトタイプはQuasar Frameworkを使用したVue.jSをAmplifyで動かす。  
UIはStripe Elementsで作る。  
認証ページはCogniteで作成。

### ■dataモデルを作成。
フライトデータ、ブッキングデータ、ロイヤリティ(ポイント)データを実値で入れていく。

その後、これをGraphQLで読み書きができるように実値を変数にする。

### ■GraphQL Transformer
ここらへんは正直よく分かんなかった。

上で作成したGraphQLデータに@modelとか@connectionとか付けていた。関数かな？

### ■支払い情報について
ページの見栄えはstripeとJavaScriptで整えていく。

ここはAmplifyじゃなくて、API Gateway　→ Lambda → Stripeってなってた。データ取ってきて表示させるだけかな。

### ■表示速度について
予約検索して、大体2，3秒で反応が返ってくる。

### ■Serverサイドのキャッシングについて
AppSyncの設定を変更すればOK。

### ■ログについて
それぞれのアプリページのログはCloud watchのカスタムメトリクスで作る。ちゃんと動いてるかとか。

AppSyncのログはCloud watch Logs Insightを使う。

### ■セキュリティについて
フロントエンドのパラメータコードは全て変数な為、問題無し。  
(普通のアプリはそうなんじゃ…？)

あとセキュリティ用HeaderをBuildに含めると、不審なIPや何度もアクセスしてくる輩を弾けるとのこと。

### ■ハイレベルアーキテクチャ
スライドのスクリーンショット。訳ワカメ。  
![スクショ](../../img/IMG_4560.JPG)

### ■アプリは以下githubに公開中
https://github.com/aws-samples/aws-serverless-airline-booking

### ■最後に
近年ビジネスでの利用状況はvueがJavaScriptの2倍近く使われている。

 ビジネスを見据えるならまずはサーバレスを推進すべきだ。  
### **それを増幅させろ(Amplify it)！**
フロントエンドのモジュール化だ。

### ■感想
社内の便器状況システムに足りなかった、便器予約システムをこれで作ってみたらいいかも。  
便器ブッキング、ベンキングかな。
