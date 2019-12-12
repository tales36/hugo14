---
title: "CMP302_AWS_Outposts_Extend_The_AWS_Experience_To_On_Premises_Environments"
date: 2019-12-05T09:43:27+09:00
author: "katsutoshi miyata"
tags: ["勉強系","AWS re:invent2019"]
cover: ../../img/awsreinvent2019.jpg
---

## ■AWS Outpostsとは
### ◆これを送りつけます。
![outpost](../../img/IMG_4720.JPG)    

## ■AWSをオンプレミスに持っていこう
### ◆Outposts Rack
AWSと同じ構成のハードウェアインフラで、Nitro systemが組み込まれてる＝EC2などの基盤が使える。

### ◆フルマネージド監視と運用はAWSが対応
同じリージョン内に限り

### ◆操作について
シングルPaneの管理が可能。通常と同じAPIとツールが使える。

## ■なんで今さら？
AWSの利点はまず、インフラ構築が容易なところ。  
故にマイクロサービスだって迅速に提供することが出来る。  
ポリシー上、クラウドにデータを置けない医療関係や公共関係のお客様が対象。

## ■Outpostsの利用方法
### ◆利用概要
使い方は、AWS Cloud側にOutpost Proxiesを準備し、データセンターにはOutposts Edge Deviceを置く。  
　→EdgeはProxiを経由してAWS Cloudとデータセンターを行き来する。

AWS outpostsはクラウド版AWSと同じコントロールパネル、同じNitroハード、ソフトウェア、同じAWS経験をあなたに与えてくれる。

### ◆ネットワーキング
同じVPCの別サブネットとしてDCの拠点を使うことが出来る。

### ◆依頼方法
1. AWSのサイトでプロダクトを作成。  
2. ロケーション、性能、ネットワーク設定、weight Requirementsを設定。
3. outpostsの種類を選ぶ（多分EdgeDeviceかRack？）
4. 使用するコンピュートとEBSなど、必要情報を入力
5. submit!!

あとはOutposts技術担当者がやりとりしてくれる

### ◆ハードウェア修理
全ての障害、ラックのコンポーネントの冗長性、リプレイススケジュールもAWSが対応。  
それらがoutpostsのコストの中に入ってるから。

### ◆Nitro Security Key
全てのデータは暗号化されてる。Nitro上の。  
鍵マテリアルはリムーバルデバイスで保持されている。  
エターナルキーでラッピングされている。  
![key1](../../img/IMG_4726.JPG)    
![key2](../../img/IMG_4727.JPG)  

## ■outpostを使ってみよう
### ◆Amazon ECS
クラスターのうち一つのコンテナをoutpost上でデプロイ。他はCloud上。

### ◆Amazon EKS
Worker NodeをDCに置く。コントロールPlaneはCloud上でデプロイ。

### ◆coming soon情報
S3が対応するかも。

## ■カスタマー事例
### ◆フィリップス
ヘルスケア分野でoutpostsを利用
診断の際の患者の情報などをoutpost上で通信させている。

## ■感想
日本で最初聞いた時にピンとこなくて、今回聞いてようやく理解した。  
今回の主題にもなってるように、ヘルスケア分野に進出しようとしているAWSの一石サービスでした。  
エッジで処理させる為なのかな…と考えてたのは若干的外れだったみたい。

あと、Rack単体でどれだけ料金かかるのか気になったり。  
デバイス好きは食らいつきそう。