---
id: notification
title: Notification
sidebar_label: Notification
---

## Overview

Notification は、ポップアップの通知を表示します。

<iframe src="https://kuc-storybook.netlify.app/iframe.html?id=notification--documentinfo" title="notification info image" height="70px"></iframe>

<iframe src="https://kuc-storybook.netlify.app/iframe.html?id=notification--documentsuccess" title="notification success image" height="70px"></iframe>

<iframe src="https://kuc-storybook.netlify.app/iframe.html?id=notification--documenterror" title="notification error image" height="70px"></iframe>

---

## Specification

### Property

使用できるプロパティの一覧です。プロパティを指定して値を更新することができます。

| Name | Type | Default | Description | Remark |
| :--- | :--- | :--- | :--- | :--- |
| className | string | "" | コンポーネントの class 名 ||
| text | string | "" | 表示するテキスト ||
| type | string | "danger" | 背景色 | 以下を指定できる<br>"danger" : Red(#e74c3c)<br>"info" : Blue(#3498db)<br>"success" : Green(#91c36c) |

### Constructor

Notification(options)
使用できるコンストラクタの一覧です。

#### Parameter
| Name | Type | Default | Description | Remark |
| :--- | :--- | :--- | :--- | :--- |
| options | object | {} | コンポーネントのプロパティを含む JSON オブジェクト | options 内の値は任意 |

### Method

使用できるメソッドの一覧です。

#### open()
Notification を表示する

##### Parameter
none

##### Return
none

#### close()
Notification を非表示にする

##### Parameter
none

##### Return
none

---
## Sample Code

全てのパラメータを指定した場合のサンプルコードです。

```javascript
const notification = new Kuc.Notification({
  text:  'Error occurred!',
  type: 'danger',
  className: 'options-class'
});
notification.open();
notification.close();
```
