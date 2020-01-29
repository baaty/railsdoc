---
layout: page
---
### 説明
検索ボックスを生成

### 使い方
    search_field_tag(要素名 [, 値, オプション])

### オプション

オプション   | 説明
---------- | ------------------
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
    search_field_tag 'name'
    # <input id="name" name="name" type="search" />

    search_field_tag 'search', 'Enter your search query here'
    # <input id="search" name="search" type="search" value="Enter your search query here" />

    search_field_tag 'search', nil, class: 'special_input'
    # <input class="special_input" id="search" name="search" type="search" />

    search_field_tag 'search', 'Enter your search query here', class: 'special_input', disabled: true
    # <input disabled="disabled" class="special_input" id="search" name="search" type="search" value="Enter your search query here" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L626)