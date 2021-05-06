---
id: version-1.0.0-button
title: Button
sidebar_label: Button
original_id: button
---

## Overview

Button は、ボタンを表示します。

<iframe src="https://kuc-storybook.netlify.app/iframe.html?id=button--document" title="button image" width="550px" height="80px"></iframe>

---

## Specification

### Property

使用できるプロパティの一覧です。プロパティを指定して値を更新することができます。

| Name | Type | Default | Description | Remark |
| :--- | :--- | :--- | :--- | :--- |
| className | string | "" | コンポーネントの class 名 |  |
| id | string | "" | コンポーネントの id 名 |  |
| text | string | "" | ボタンに表示するテキスト ||
| type | string | "normal" | ボタンのデザインタイプ | 以下を指定できる<br>"normal" : Gray(#f7f9fA)<br>"submit" : Blue(#3498db)<br>"alert" : Red(#e74c3c) |
| disabled | boolean | false | コンポーネントの編集可/不可設定 ||
| visible | boolean | true | コンポーネントの表示/非表示設定 ||

### Event

指定できるイベントの一覧です。

| Name | Type | Description | Remark |
| :--- | :--- | :--- | :--- |
| click | function | クリックされた時のイベントハンドラ | 引数には Event の event オブジェクトをとる |

### Constructor

Button(options)
使用できるコンストラクタの一覧です。

#### Parameter

| Name | Type | Default | Description | Remark |
| :--- | :--- | :--- | :--- | :--- |
| options | object | {} | コンポーネントのプロパティを含む JSON オブジェクト | options 内の値は任意 |

---

## Sample Code

全てのパラメータを指定した場合のサンプルコードです。

<script src="https://gist.github.com/phongnm-dev/eb86519d5fe976631a442d3747f5d4e2.js"></script>
