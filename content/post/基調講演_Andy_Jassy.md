---
title: "基調講演_Andy_Jassy"
date: 2019-12-04T03:49:23+09:00
author: "katsutoshi miyata"
tags: ["勉強系","AWS re:invent2019"]
cover: ../../img/awsreinvent2019.jpg
---

## ■今回のAWS re:inventについて
### **参加者は65000人。** セッション数は3000人を越えた。

## ■マーケット情報

いまだに世界規模だと97%がオンプレを利用。  
クラウド利用者の3%のうち、47.80%がAWSで15%がMS、アリババが7.7％、Googleが5%

相変わらずAWSが一強なのは想定通りとして、アリババがGCP抜かしてるの草  
やはり、トップメタを追うのが板。

## ■EC2関連の新しいサービス
### ◆M6g、R6g、C6gファミリー
カスタマイズされたCPU(5世代の子比べると4倍)と、25Gbpsのエンハンスドネットワークが利用可能。

### ◆inf1ファミリー
マシンラーニング用にチューンされたインスタンス。
GPUを積んでるG4ファミリーより低レイテンシーで3倍速いスループットなのに、4割安い。

## ■AWS Fargate for Amazon EKS
待ちに待ったFargateのEKS対応。

## ■Amazon Sage Maker
### SageMaker Studio
![SMS](../../img/IMG_4597.JPG)  
WEBベースのマシンラーニングIDE

### SageMaker Notebooks
![SMN](../../img/IMG_4599.JPG)
インスタンス無しに、ワンクリックでNotebookを作成。

### SageMaker Experiments
![SME](../../img/IMG_4600.JPG)
ML結果を自動でキャプチャしてくれる。キャプチャしたデータはSageMaker Studioで見れる。

### SageMaker Debugger
![SME](../../img/IMG_4604.JPG)
自動でトレーニングメトリクスとかをデバッグしてくれる。

### SageMaker Model Monitor
![SME](../../img/IMG_4606.JPG)
MLモデルの監視ができる機能っぽい。

### SageMaker AutoPilot
![SME](../../img/IMG_4608.JPG)
ML作業の自動化。S3かSageMaker StudioにCSVデータ入れたら自動で変換してくれたり、モデル選んでくれたりしくれるみたい。

## Amazon CodeGuru
![ACG](../../img/IMG_4614.JPG)
コードを放り込んだら ~~勝手に~~自動でレビューしてくれる。これ良さそう。

## ■Amazon Kendra
いろんなパブリックストレージから、インデックスを作成してFAQ形式で出力してくれるサーチエンジン。  
GDriveに標準でついてるやつ。  

BOXとかDropboxとかの有名どころには大体対応してたから、GDriveじゃなくても **"超優秀な検索エンジンがあるんだから、フォルダ分けしないでいいよね精神"** が使えて便利そう。

## ■感想
生でAndy Jassyの基調講演見れて良かった。
AWSの最新情報を日本に居る誰よりも早く仕入れられるのが最高なんじゃしぃ。

今年は機械学習周りのアップデートが多くて、生Matt Woodも見れたし満足。  
イケメンは目の保養。カッコいい。