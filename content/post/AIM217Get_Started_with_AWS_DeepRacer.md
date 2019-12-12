---
title: "AIM217Get_Started_with_AWS_DeepRacer"
date: 2019-12-03T09:03:56+09:00
author: "katsutoshi miyata"
tags: ["勉強系","AWS re:invent2019"]
cover: ../../img/awsreinvent2019.jpg
---

## DeepRacer Workshop
### ■**AWS DeepRacer Evo** リリースの報告

カメラが二つ付いて、光センサーが新たに付いた。  
→それに伴い、オブジェクトに対する遠近などを報酬にする関数も何個か追加。

![dr](../../img/dr.jpg)

### ■2020AWS Deep Racer League
2020年はもっと開催数増やすらしい。現状年一回のSummitとre:inventだけなので。  
あと、Community Racesという身内だけで出来るモードが追加された。

### ■2019DeepRacer League(実際のコース版)
7.44sの日本人のレーサーが世界レコード1位。  
仮想コースと違って機体の抵抗とか摩耗なども計算しないといけない為、これが世界レベルの国が日本というのは誇らしい。

### ■ML Overview
ここら辺の話は前受けたWorkshopとほぼ一緒。

https://days.19900119.xyz/post/deepracerworkshop20191018/

の、強化学習～座標系と参照点までを見てほしい。

### ■Example Paramater
ALL_wheeles
　→すべての車輪がコースに入ってればTrue。外れてればfalseで強化学習する。

distance_Center
　→センターラインからの距離で報酬を変化させる。

### ■ガレージ機能
DeepRacerコントロールパネルのアップデート。  
自分の仮想ヴィークルを自由に作成できる。  
　→旧機体か、今回のEvoを選択できるように。光センサーの有る無しも。

### ■Workshop
内容も日本とほぼ一緒。  
ガレージ機能を使ってみようねというセクションが追加されてた。  
報酬関数については、光センサー関連のがいくつか追加されてる。  
オブジェクトから近いとか遠いとか。

### ■githubはこちら
https://github.com/aws-samples/aws-deepracer-workshops

### ■Go Race
MGM Grand Garden
　→敗者復活戦リーグ
　→自分のモデル走らせられる
　→DeepRacer Evoのお試し会

Quad at Aria
　→Deep Racer bootcamp

Venetian
　→最終戦を火曜日にやる。

### ■MLについてもっと学ぼう
70を越えるAWS公式のML学習コース。  
AWS認定マシンラーニングスペシャルティ試験。

### ■感想
DeepRacer今年も貰えるんかなって思ったらそんなに甘くなかった。  
日本でやったBootcampまんまって感じだったけど、アップデート情報もあったので満足。  
ついでに学習中のMiyaTurbo2号機見て見て。

![deepracer](../../img/deepracer.gif)

明日DeepComposerのWalkupチャレンジしてみるかなぁ。