---
layout: page
---
### 説明
ページ全体ではなく、ページの一部をキャッシュするときに使う

### 使い方
    <% cache([キャッシュキー, オプション]) do %>
      キャッシュ
    <% end %>

### オプション

オプション     | 説明
------------ | --
:skip_digest | digestの付与をスキップ

### 例
    <% cache [ project, current_user ] do %>
      <b>All the topics on this project</b>
      <%= render project.topics %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/cache_helper.rb#L166)