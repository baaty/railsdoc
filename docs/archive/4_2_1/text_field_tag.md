---
layout: page
---
### 使い方
    text_field_tag(要素名 [, 値, オプション])

### 使用できるフォームタグ
* form_for

### オプション

オプション        | 説明
------------ | ------------------
:disabled    | フォームの項目の利用禁止
:size        | フォームの幅
:maxlength   | 入力フィールドに入力可能な最大文字数
:placeholder | プレスホルダー
:accept      | フォームで受付可能なMIMEタイプ
:readonly    | フォームの内容変更禁止
:tabindex    | Tabキーによる入力欄の移動順
:accesskey   | フォームに移動するショートカットキー
:id          | 要素固有の識別子
:class       | 要素を分類するクラス名
:title       | 要素の補足情報
:style       | 要素の補足情報
:dir         | 表記方向
:lang        | 基本言語

### 例
#### 初期値なし
    <%= text_field?tag 'page[name]' %>
    # <input id="page_name" name="page[name]" type="text" />

#### 初期値あり
    # @page.name = "abc"
    <%= text_field_tag 'page[name]' %>
    # <input id="page_name" name="page[name]" type="text" value="abc" />

#### class属性を指定
    <%= text_field_tag 'page[name]', :class = 'page_name' %>
    # <input class="page_name" id="page_name" name="page[name]" type="text" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L188)