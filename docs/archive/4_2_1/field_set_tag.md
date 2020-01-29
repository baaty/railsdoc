---
layout: page
---
### 説明
モデルを固定してフォームを生成。form_for内で異なるモデルを編集できるようになる

### 使い方
    <%= field_set_tag(サブフォームのタイトル [, オプション]) do %>
    <% end %>

### 使用できるフォームタグ
* form_for
* form_tag

### 例
#### サブフォームがCategory
    <%= field_set_tag 'Category' do %>
      <%= text_field_tag 'name' %>
    <% end %>
    # <fieldset><legend>Category</legend><input id="name" name="name" type="text" /></fieldset>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L556)