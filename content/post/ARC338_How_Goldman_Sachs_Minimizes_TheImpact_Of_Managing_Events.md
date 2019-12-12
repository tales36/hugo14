---
title: "ARC338_How_Goldman_Sachs_Minimizes_TheImpact_Of_Managing_Events"
date: 2019-12-05T10:26:45+09:00
author: "katsutoshi miyata"
tags: ["勉強系","AWS re:invent2019"]
cover: ../../img/awsreinvent2019.jpg
---

## ■はじめに
### ◆優秀な運用とは
フローの自動化を進め、ビジネスの価値を届け続けるという事。
その為に以下を常に推進し続ける必要がある。

1. コードによる運用を徹底する
2. 運用手順を見直す
3. 失敗を予測する
4. 運用失敗事例すべてから学ぶ

### ***Design with Ops in Mind***(カッコいいロゴ)

## 使用しているサービス
### ◆AWS Cloud trail
　→オペレーションログを残せるので、後の振り返りに大いに役立つ

### ◆AWS X-Ray
　→サービスマップとこちらでコードの脆弱性の追跡ができる。

### ◆Amazon CloudWatch
Alarm Event(time)、Event(event)、Rule
 →上記全てをEvent Bridgeに。

### ◆AWS Systems Manager OpsCenter
これは上記三つのサービスとは違い、考慮すべき点が多かったとのこと。
結局Taskの振り分けをLamabdaでおこなうことになった。

## ■感想
もうちょっと面白いセッションかなって思ったら、日本でもよくある感じのセッションでした。  
運用自動化の内容ばかりで、これでどれだけ効果があったかの話が無かったので、有効かどうかはちょっと怪しい。  
Lamabda頑張って作ったってのは伝わってきたけど。

あと、オマケ。  
![bkup](../../img/IMG_4757.JPG)  

リストアも自動化してるらしい。  
![rstr](../../img/IMG_4758.JPG)  




