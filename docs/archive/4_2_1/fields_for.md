---
layout: page
---
### 説明
モデルを固定してフォームを生成。form_for内で異なるモデルを編集できるようになる

### 使い方
    <%= fields_for(モデル) do |i| %>
    <% end %>

### 使用できるフォームタグ
* form_for

### 例
#### pageモデルにcategoryモデルの情報を入力
    <%= form_for(@page) do |i| %>
      <%= fields_for @page.category do |category| %>
        <%= category.text_field :name %>
      <% end %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1572)