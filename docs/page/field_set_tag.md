---
layout: page
---
### 説明
モデルを固定してフォームを生成
form_for内で異なるモデルを編集できるようになる

### 使い方
    <%= field_set_tag(サブフォームのタイトル [, HTMLオプション]) do %>
    <% end %>

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
#### サブフォームがCategory
    <%= field_set_tag 'Category' do %>
      <%= text_field_tag 'name' %>
    <% end %>
    # <fieldset><legend>Category</legend><input id="name" name="name" type="text" /></fieldset>

#### class付与
    field_set_tag 'Compliance', class: 'rights' do
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L581)