---
layout: page
---
### 説明
モデルからDIVタグを生成

### 使い方
    div_for(モデル [, オプション])

### 例
    <%= div_for(@person, class: "foo") do %>
       <%= @person.name %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/3f2ac795b8f49ad07ec30790fe716cbdac78642c/actionview/lib/action_view/helpers/record_tag_helper.rb#L33)