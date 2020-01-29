---
layout: page
---
### 説明
モデルを固定してフォームを生成
form_for内で異なるモデルを編集できるようになる

### 使い方
    <%= fields_for(モデル) do |i| %>
    <% end %>

### 例
#### pageモデルにcategoryモデルの情報を入力
    <%= form_for(@page) do |i| %>
      <%= fields_for @page.category do |category| %>
        <%= category.text_field :name %>
      <% end %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1007)