---
layout: page
---

### 説明

キャッシュがブロック内にあるか

### 使い方

    caching?()

### 例

    <% cache project do %>
      <% raise StandardError, "Caching private data!" if caching? %>
    <% end %>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/cache_helper.rb#L188)
