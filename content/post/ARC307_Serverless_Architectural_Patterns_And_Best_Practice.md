---
title: "ARC307_Serverless_Architectural_Patterns_And_Best_Practice"
date: 2019-12-05T13:08:38+09:00
author: "katsutoshi miyata"
tags: ["勉強系","AWS re:invent2019"]
cover: ../../img/awsreinvent2019.jpg
---

## ■はじめに
### ◆サーバーレスにするメリット
サーバーレスにすると、保守の必要無く、高可用性であり、    
セキュアでパフォーマンスも出るのに費用は少なく済む。  

### ◆構成例1
ベストプラクティスな構成にはまずAWS Lambdaが必要不可欠。
データの配信、変換、サービスからサービスへの橋渡しなどなど。

例えば  
>DirectConnectからのデータをKinesis経由でLambdaからDynamoDBに登録。  

これは大量のデータ通信が必要なマシンラーニングなどの用途で使われる。

### ◆構成例2
まさかの1日目の空港アプリがここでも登場。
Amplifyっていう良いのがあってね～という話で、以下ほぼ一緒だったんで気になる人は以下リンク飛んでください。

[MOB308_Production_Grade_full_Stack_apps_with_AWS_Amplify](https://days.19900119.xyz/post/MOB308_Production_Grade_full_Stack_apps_with_AWS_Amplify/)

## ■素材リンク集
[Realworld-Serverless-Application](https://github.com/awslabs/realworld-serverless-application)

[aws-lambda-powertools](https://github.com/awslabs/aws-lambda-powertools)

## ■感想
後半戦、それもう聞いたんだけどお！って思いながら聞いてました。  
うーむ、肩透かし。  
参考リンクは上以外にもQRコードで発表されてたのもありましたので、  
そちらは後日の資料から確認してください。(写真ブレブレな為)