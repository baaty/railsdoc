---
layout: page
---

### 説明

モデルを固定してフォームを生成  
form_for内で異なるモデルを編集できるようになる

### 使い方

    fields_for(名前, モデル=nil, オプション={}, ブロック引数)

### 例

#### モデルを固定してフォームを生成  

    <%= fields_for :permission, @person.permission do |permission_fields| %>
      Admin?  : <%= permission_fields.check_box :admin %>
    <% end %>

#### 簡略化

    <%= fields_for :permission do |permission_fields| %>
      Admin?: <%= permission_fields.check_box :admin %>
    <% end %>

#### モデル自体を渡す

    <%= fields_for @person.permission do |permission_fields| %>
      Admin?: <%= permission_fields.check_box :admin %>
    <% end %>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1020)
