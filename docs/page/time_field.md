---
layout: page
---

### 説明

時間の入力欄を生成

### 使い方

    time_field(要素名, メソッド, オプション={})

    # f.object
    f.time_field(メソッド, オプション={})

### オプション

| オプション       | 説明                                         |
| ---------------- | -------------------------------------------- |
| :min             | 最少値                                       |
| :max             | 最大値                                       |
| :step            | 許容値の粒度                                 |
| :size            | フォームの幅                                 |
| :include_seconds | 出力のタイムスタンプ形式に秒とミリ秒を含める |
| :maxlength       | 入力フィールドに入力可能な最大文字数         |
| :accept          | フォームで受付可能なMIMEタイプ               |
| :readonly        | フォームの内容変更禁止                       |
| :disabled        | 無効化                                       |
| :tabindex        | Tabキーによる入力欄の移動順                  |
| :accesskey       | フォームに移動するショートカットキー         |
| :id              | 要素固有の識別子                             |
| :class           | 要素を分類するクラス名                       |
| :title           | 要素の補足情報                               |
| :style           | 要素の補足情報                               |
| :dir             | 表記方向                                     |
| :lang            | 基本言語                                     |

### 例

#### 時間の入力欄を生成

    time_field("task", "started_at")
    #=> <input id="task_started_at" name="task[started_at]" type="time" />

#### 最小値を指定

    time_field("task", "started_at", min: Time.now)
    #=> <input id="task_started_at" name="task[started_at]" type="time" min="01:00:00.000" />

#### 時間の入力欄を生成(f.time_field)

    f.time_field :started_at
    #=> <input id="task_started_at" name="task[started_at]" type="time" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1465)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1883)
