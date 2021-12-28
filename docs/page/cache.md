---
layout: page
---

### 説明

ページ全体ではなく、ページの一部をキャッシュするときに使う

### 使い方

    cache(キャッシュキー={}, オプション={}, ブロック引数)

### オプション

| オプション   | 説明                   |
| ------------ | ---------------------- |
| :skip_digest | digestの付与をスキップ |

### 例

    <% cache [ project, current_user ] do %>
      <b>All the topics on this project</b>
      <%= render project.topics %>
    <% end %>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/cache_helper.rb#L168)
