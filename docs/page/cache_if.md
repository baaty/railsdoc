---
layout: page
---

### 説明

条件式がtrueの時にキャッシュ

### 使い方

    cache_if(条件式, キー名={}, オプション={}, ブロック引数)

### 例

    <% cache_if admin?, project do %>
      <b>All the topics on this project</b>
      <%= render project.topics %>
    <% end %>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/cache_helper.rb#L215)
