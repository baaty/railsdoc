---
layout: page
---
### 説明
メールアドレス入力ボックスを生成

### 使い方
    email_field_tag(要素名 [, value値, オプション or HTMLオプション])

### オプション

オプション        | 説明
-------------|--------------------
:disabled    | 無効化
:size        | フォームの幅
:maxlength   | 入力フィールドに入力可能な最大文字数
:placeholder | フォーカスが当たるまで表示される文字列

### HTMLオプション

オプション      | 説明
-----------|-------------------
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### 例
#### メールアドレス入力ボックスを生成
    email_field_tag 'name'
    # <input id="name" name="name" type="email" />

#### 初期値
    email_field_tag 'email', 'email@example.com'
    # <input id="email" name="email" type="email" value="email@example.com" />

#### classを付与
    email_field_tag 'email', nil, class: 'special_input'
    # <input class="special_input" id="email" name="email" type="email" />

#### 無効化
    email_field_tag 'email', 'email@example.com', class: 'special_input', disabled: true
    # <input disabled="disabled" class="special_input" id="email" name="email" type="email" value="email@example.com" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L757)