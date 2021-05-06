---
id: version-1.0.0-search-box-customization
title: 検索ボックスカスタマイズ
sidebar_label: 検索ボックスカスタマイズ
original_id: search-box-customization
---

## 概要
検索ボックスの作り方を kintone UI Component の Text コンポーネントと Button コンポーネント、Notification コンポーネントを使って説明します。

## 完成イメージ
検索ボックスの完成イメージは、次の通りです。

#### デスクトップ版
![検索ボックス(デスクトップ)](assets/desktop_search_box.png) 

#### モバイル版
![検索ボックス(モバイル)](assets/mobile_search_box.png) 

## JavaScript/CSS カスタマイズ

kintone UI Component の UMD ファイルをアプリに読み込んだ上で、以下のような実装をした JavaScript ファイルをアップロードします。  
ファイルのアップロード方法などは、 [Quick Start](../getting-started/quick-start.md) をご覧ください。

### 検索ボックスの表示

検索ボックスを表示するために、Text コンポーネントと Button コンポーネントを使います。  
Text コンポーネントの placeholder プロパティを使うと、入力内容を説明することができます。  
モバイル対応をしたい場合は、モバイル用のコンポーネント MobileButton を呼び出すと同じように実装できます。  

<script src="https://gist.github.com/phongnm-dev/c0c464e63df6b0c4192fe0ebb4c1b9a4.js"></script>

### 検索文字のチェック

Button コンポーネントは、click イベントを指定することができます。  
ここでは以下のような処理を入れています。

- ボタンをクリックした時に、入力された文字が全角文字か判定
- 入力値が全角以外の場合、error プロパティにエラーメッセージを代入して表示
- error プロパティに空文字を代入して、表示メッセージを初期化

<script src="https://gist.github.com/phongnm-dev/45c04e663b38a02c27475f0bb5868bc2.js"></script>

### コンポーネントの増殖バグ対策

id プロパティを付与して、既にコンポーネントが表示されているかどうかを判定し、増殖バグを防ぐ対応をしています。

<script src="https://gist.github.com/phongnm-dev/49847f2700d50a037bae4ff16c10bb31.js"></script>

### 実行結果を Notification で表示

REST API 実行時の成功や失敗のメッセージを Notification コンポーネントを使って表示します。  
Notification の呼び出しには open メソッド、背景色の設定には type プロパティを使っています。  
今回は、以下のケースで表示するように実装しています。  

- レコードの結果がない場合
- REST API の実行が失敗した場合

<script src="https://gist.github.com/phongnm-dev/5e38565c747275d28a83d6595484f205.js"></script>

## おわりに

いかがでしたでしょうか。kintone UI Component を使って、検索ボックスの作り方を紹介しました。  
kintone UI Component を使って、便利に kintone カスタマイズを開発していただければ幸いです。

> 本記事は、 2021 年 2 月時点の kintone と Google Chrome で確認したものになります。  
> また、カスタマイズに使用した kintone UI Component のバージョンは、v1.0.0 です。
