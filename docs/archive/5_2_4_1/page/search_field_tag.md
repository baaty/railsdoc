---
layout: archive_page
---
### 説明
モデルと関連のない検索ボックスを生成

### 使い方
    search_field_tag(要素名 [, value値, オプション])

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
#### 検索ボックスを生成
    search_field_tag 'name'
    # <input id="name" name="name" type="search" />

#### value値を設定
    search_field_tag 'search', 'Enter your search query here'
    # <input id="search" name="search" type="search" value="Enter your search query here" />

#### class属性を付与
    search_field_tag 'search', nil, class: 'special_input'
    # <input class="special_input" id="search" name="search" type="search" />

#### 無効化
    search_field_tag 'search', 'Enter your search query here', class: 'special_input', disabled: true
    # <input disabled="disabled" class="special_input" id="search" name="search" type="search" value="Enter your search query here" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_tag_helper.rb#L623)