---
layout: page
---
### 説明
ファイル選択ボックスを生成

### 使い方
    file_field_tag(要素名 [, オプション])

### 使用できるフォームタグ
* form_for
* form_tag

### オプション

オプション      | 説明
---------- | ------------------
:disabled  | フォームの項目の利用禁止
:multiple  | 複数選択可能
:accept    | フォームで受付可能なMIMEタイプ
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
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
#### オプションなし
    <%= file_field_tag 'page[fine_name]' %>
    # <input id="page_fine_name" name="page[fine_name]" type="file" />

#### class属性を指定
    <%= file_field_tag 'page[fine_name]', :class = 'page_fine_name' %>
    # <input class="page_fine_name" id="page_fine_name" name="page[fine_name]" type="file" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L272)