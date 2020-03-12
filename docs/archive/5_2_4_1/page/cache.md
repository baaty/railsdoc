---
layout: archive_page
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
#### ページの一部をキャッシュ
    <% cache [ project, current_user ] do %>
      <b>All the topics on this project</b>
      <%= render project.topics %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/cache_helper.rb#L166)