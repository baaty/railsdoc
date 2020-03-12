---
layout: archive_page
---
### 説明
時間の入力欄を生成

### 使い方
    time_field(要素名 [, 値, オプション])

### オプション

オプション   | 説明
---------- | ------------------
:min       | 最少値
:max       | 最大値
:step      | 許容値の粒度
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:disabled  | 無効化
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### 例
#### 時間の入力欄を生成
    time_field("task", "started_at")
    # <input id="task_started_at" name="task[started_at]" type="time" />

#### 最小値を指定
    time_field("task", "started_at", min: Time.now)
    # <input id="task_started_at" name="task[started_at]" type="time" min="01:00:00.000" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_tag_helper.rb#L733)