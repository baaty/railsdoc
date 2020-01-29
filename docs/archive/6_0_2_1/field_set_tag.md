---
layout: page
---
### 説明
モデルを固定してフォームを生成
form_for内で異なるモデルを編集できるようになる

### 使い方
    <%= field_set_tag(サブフォームのタイトル [, オプション]) do %>
    <% end %>

### 例
#### サブフォームがCategory
    <%= field_set_tag 'Category' do %>
      <%= text_field_tag 'name' %>
    <% end %>
    # <fieldset><legend>Category</legend><input id="name" name="name" type="text" /></fieldset>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L581)