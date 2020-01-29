---
layout: page
---
### 説明
ページ全体ではなく、ページの一部をキャッシュするときに使う

### 使い方
    <% cache([キャッシュキー]) do %>
      キャッシュ
    <% end %>

### オプション

オプション     | 説明
------------ | --
:skip_digest |

### 例
    <% cache [ project, current_user ] do %>
      <b>All the topics on this project</b>
      <%= render project.topics %>
    <% end %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/26d91f1722ef77caf0ed8e1800a773c64787397e/actionview/lib/action_view/helpers/cache_helper.rb#L113)