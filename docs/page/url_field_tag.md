---
layout: page
---
### 使い方
    url_field_tag(要素名 [, value値, オプション])

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
    url_field_tag 'name'
    # <input id="name" name="name" type="url" />

    url_field_tag 'url', 'http://rubyonrails.org'
    # <input id="url" name="url" type="url" value="http://rubyonrails.org" />

    url_field_tag 'url', nil, class: 'special_input'
    # <input class="special_input" id="url" name="url" type="url" />

    url_field_tag 'url', 'http://rubyonrails.org', class: 'special_input', disabled: true
    # <input disabled="disabled" class="special_input" id="url" name="url" type="url" value="http://rubyonrails.org" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L736)