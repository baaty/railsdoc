---
layout: page
---
### 説明
モデルからタグを動的に生成する
HTMLとERBが混ざってしまう場合などに使用するとすっきり表現できる

### 使い方
    content_tag_for(タグの名前, モデル [, オプション])

### 例
    <%= content_tag_for(:tr, @person) do %>
      <td><%= @person.first_name %></td>
      <td><%= @person.last_name %></td>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/3f2ac795b8f49ad07ec30790fe716cbdac78642c/actionview/lib/action_view/helpers/record_tag_helper.rb#L83)